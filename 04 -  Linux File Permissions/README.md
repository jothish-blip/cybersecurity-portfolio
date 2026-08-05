# Linux File Permission Management

## Overview

As part of an internal access review, I audited file and directory permissions in a Linux Bash environment. The objective was to identify permissions that no longer matched the organization's security policy and update them without affecting legitimate user access. Throughout the exercise, I reviewed existing permissions, removed unnecessary access, and verified every change before moving to the next task.

---

# Reviewing the Existing Permissions

Before making any changes, I wanted to understand the current permission settings across the project directory.

```bash
ls -la
```

<div align="center">

<img src="images/01-ls-la-output.png" alt="Directory listing before modifying permissions" width="90%">

<p><em>Figure 1 — Initial directory listing showing files, directories, hidden files, and their existing permissions.</em></p>

</div>

Running `ls -la` immediately showed every file and directory, including hidden files that a normal `ls` command would not display. That turned out to be important because one of the files I needed to update, `.project_x.txt`, is hidden.

Looking through the permission strings also gave me a quick overview of which files already matched the security policy and which ones needed attention.

---

# Understanding the Permission String

Every file and directory in Linux has a 10-character permission string that defines who can access it and what actions they can perform.

Example:

```text
-rwx---r--
```

Here's how I interpreted it:

- The **first character** indicates the file type. A `-` represents a regular file, while `d` represents a directory.
- The **next three characters (`rwx`)** belong to the file owner, granting full read, write, and execute access.
- The **following three characters (`---`)** represent the group permissions. Since all three positions are hyphens, the group has no access.
- The **last three characters (`r--`)** apply to everyone else. Others can read the file but cannot modify or execute it.

Once I understood how each section mapped to the owner, group, and others, it became much easier to identify exactly which permissions needed to change.

---

# Removing Write Access from Others

During the review, I noticed that `project_k.txt` still allowed write access that wasn't required under the updated security policy. The organization wanted users outside the owner and group to have read-only access.

To fix this, I removed write permission for others.

```bash
chmod o-w project_k.txt
ls -la
```

<div align="center">

<img src="images/02-project-k-chmod.png" alt="Removing write permission from project_k.txt" width="90%">

<p><em>Figure 2 — Verifying that write permission for others has been removed from <code>project_k.txt</code>.</em></p>

</div>

I used symbolic notation because I only needed to remove a single permission without recalculating the entire permission set using octal values.

After running `ls -la` again, the updated permission string confirmed that write access for others had been removed while every other permission remained unchanged.

---

# Updating an Archived Hidden File

The next file I reviewed was `.project_x.txt`, which had recently been archived by the research team.

Because the filename starts with a period (`.`), it doesn't appear in a normal directory listing. Using `ls -la` earlier ensured I could locate and verify the file before making any changes.

According to the updated policy:

- The owner should no longer have write permission.
- The group should no longer have write permission.
- The group should still retain read access.

I updated the permissions using the following command.

```bash
chmod u-w,g-w,g+r .project_x.txt
ls -la .project_x.txt
```

<div align="center">

<img src="images/03-hidden-file-permissions.png" alt="Updated permissions for hidden file" width="90%">

<p><em>Figure 3 — Updated permission string for the archived hidden file <code>.project_x.txt</code>.</em></p>

</div>

I chose symbolic notation (`u-w,g-w,g+r`) because it lets me target only the permission bits that need to change instead of replacing the complete permission mode.

A quick verification confirmed that the file permissions now matched the organization's retention policy.

---

# Restricting Access to the `drafts` Directory

The final task involved securing the `drafts` directory.

Only the `researcher2` account should be able to access the directory and its contents. The group no longer required execute permission, so I removed only that permission while leaving the owner's access unchanged.

```bash
chmod g-x drafts
ls -ld drafts
```

<div align="center">

<img src="images/04-directory-permission.png" alt="Updated directory permissions" width="90%">

<p><em>Figure 4 — Final permission settings for the <code>drafts</code> directory after removing group execute access.</em></p>

</div>

Since the owner already had the required permissions, there was no reason to modify them. Keeping the change as small as possible reduced the chance of accidentally affecting legitimate access.

Running `ls -ld drafts` confirmed that the group execute bit had been removed while `researcher2` retained the required permissions.

---

# Conclusion

This project gave me hands-on experience working with Linux file permissions and access control using Bash. Instead of applying broad permission changes, I updated only the permissions that needed adjustment and verified each change before moving on.

Reviewing the existing permissions first, making targeted updates with `chmod`, and confirming the results afterward reinforced the importance of the principle of least privilege. Even small permission changes can significantly improve system security while ensuring authorized users continue to have the access they need.
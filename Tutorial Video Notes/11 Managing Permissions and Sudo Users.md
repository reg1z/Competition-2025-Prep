# Video 11
https://www.youtube.com/watch?v=to0GrfGERK0&list=PLqux0fXsj7x3WYm6ZWuJnGC1rXQZ1018M&index=11

- **Understanding File Permissions**
    - `ls -l` displays file **permissions**, owner, and group.
    - Permissions are divided into **owner, group, and others**.
    - `rwx` represents **read (r), write (w), and execute (x)** permissions.
- **Modifying File Permissions**
    - `chmod <permissions> <file>` changes file permissions.
    - Numeric mode: `chmod 777 <file>` grants **full access**.
    - Symbolic mode: `chmod u+w <file>` adds **write permission** for the owner.
- **Changing File Ownership**
    - `chown <user>:<group> <file>` assigns a new owner and group.
    - `sudo` is required to change ownership of files **not owned by the user**.
- **Understanding Sudo Privileges**
    - `sudo <command>` runs a command with **administrator privileges**.
    - Users must be **listed in the sudoers file** to execute `sudo`.
    - `visudo` is used to **edit the sudoers file** safely.
- **Managing Access Restrictions**
    - `chmod 700 <directory>` allows **only the owner** to access a folder.
    - Removing write permissions restricts users from **modifying files**.
    - Group and user permissions define **who can access and modify data**.


# Video 10
![](https://www.youtube.com/watch?v=rR_n2ciilrc&list=PLqux0fXsj7x3WYm6ZWuJnGC1rXQZ1018M&index=8)

- **Checking Your Current User**
    - `whoami` displays the **current logged-in user**.
    - Important for **multi-user systems** to track identities.
- **Creating a New User**
    - `adduser <username>` creates a new user account.
    - Requires **root privileges**, so `sudo adduser <username>` is necessary.
    - Prompts for a **password** and optional personal details.
- **Understanding Home Directories**
    - New users get a home directory at `/home/<username>`.
    - Default settings may vary depending on the system.
- **Switching Users**
    - `su <username>` switches to another user.
    - Prompts for the **target user’s password**.
    - File paths may change depending on the user’s **home directory**.
- **User Permissions**
    - User access and security depend on **permissions**.
    - Some actions require **administrator privileges** (`sudo`).


---
#### Next in Playlist: [[11 Managing Permissions and Sudo Users]]
# Video 13
https://www.youtube.com/watch?v=BJJBSUe5JEk&list=PLqux0fXsj7x3WYm6ZWuJnGC1rXQZ1018M&index=13

- **Understanding User Groups**  
	- Every user belongs to at least **one group**, often named after the user.  
	- Groups help manage **permissions** for multiple users.  
	- `groups` command shows **all groups** a user belongs to.  
- **Checking Group Memberships**  
	- `groups <username>` lists a specific user’s groups.  
	- `id <username>` provides **numeric group IDs (GIDs)**.  
- **Managing User Groups**  
	- `sudo usermod -aG <group> <user>` adds a user to a group.  
	- `sudo gpasswd -d <user> <group>` removes a user from a group.  
	- Users must **log out and back in** for group changes to take effect.  
- **Viewing System Groups**  
	- `/etc/group` file lists **all groups and their members**.  
	- `cat /etc/group` displays the **group database**.  
- **Granting Sudo Access Through Groups**  
	- Users in the `sudo` group can execute **admin commands**.  
	- `sudo usermod -aG sudo <user>` grants **sudo privileges**.
	- Users must belong to a **group listed in `/etc/sudoers`** to run `sudo` commands.  
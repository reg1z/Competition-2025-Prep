# NCAE-2025-Prep
## Relevant Links
- Competition Rules https://www.ncaecybergames.org/rules/
- NCAE Discord https://discord.ncaecybergames.org/
- Questions answered by NCAE staff (Discord)
	- "What is the line where an online service must be disclosed?" https://discord.com/channels/624969095292518401/1339009691044544542
	- 

---

**(⭐ = really important omg)**

## Pre-Game
### SPICE config | Shared Clipboard (copy/paste) & Automatic Screen Resizing

**TO PREPARE:**
- Install `virt-viewer` on the PC / VM you'll be using to compete.
	- **Link (scroll down):** https://virt-manager.org/download
		- .MSI installer for Windows
		- .tar.xz for UNIX
	- Available on the default repos in most popular Linux distros via package manager install (`apt` / `yum` / `dnf` / `pacman` / etc... )

**ON GAME DAY:**
- Enable the **spice-vdagent** on necessary hosts.
	- ***NOTE:** Only applied to Kali hosts in both Mini Hack challenges (this could be different on game day)*
- It should work once enabled after relogging in.
- ⭐ How to make sure the spice-vdagent is enabled systemwide in the background, available to all users logging in? Or is it per user account?
Commands:
```bash
sudo systemctl enable spice-vdagent
sudo systemctl start spice-vdagent
```

---

## Potential System Hardenings

### Least privilege
- Configure user accounts with unique secure passwords for each member of the team?
	- Should each have sudo/root access?
		- If so, should the sudo password for each be unique?
- ⭐ Change User/Password defaults
	- ⭐ Microtik Router
	- Webserver
	- Kali Machines
	- ???
	- Remove / Disable / Change PWs of any default user accounts

### Automated secure remote backups
- ***Potential Solutions***
	- `rsync` + `ssh` (with PKI keys) + `cron` (taught in NCAE YouTube playlist)
		- Use proper nesting of the `ssh` command in quotes when using rsync via ssh w/ keys (`"ssh -i keyfile"`).
		- What method to use to transfer key(s) to target systems?
		- keep ssh keys for the automated backup using the root account in a separate root-only readable folder?
- ***Should there be backups of...***
	- ssh keys for passwordless access?
	- Entire systems?
		- webserver?
		- router? (How feasible is this w/ the microtik router?)
		- other (???)
- Where should backups be stored? On which host(s)? Multiple hosts?
- Is *encrypting* backups feasible—i.e. is there enough time and compute resources?

### Monitoring
- LOGS 🎶🎸🌲🪓🎸🎶
- ???

### Known Unknowns
- ***Network Topology***
	- IPs (team number) + Netmasks
- ***We will have external internet access, therefore...***
	- Will we need to patch any systems?
		- This could involve running vulnerability scans and deploying patches.
		- If patches are unavailable, will require implementation of compensating controls.
- ***Specific Host Information***
	- How many hosts are in our control?
	- What OS/distro/software do they have?
	- ⭐ ***Services***
		- Which services are configured by default?
		- Which services increase our attack surface?
		- What services are necessary to accomplish our goal(s)?
		- Which services have widely-known default values?
	- ⭐ ***Router***
		- What's allowed through by default?
		- What do we allow through?
		- What do we block?

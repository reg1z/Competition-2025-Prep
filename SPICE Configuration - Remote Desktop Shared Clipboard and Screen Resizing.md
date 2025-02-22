# SPICE Config
*Shared Clipboard (copy/paste) & Automatic Screen Resizing*

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
# Video 20
![](https://www.youtube.com/watch?v=3vbFNmnJCl0&list=PLqux0fXsj7x3WYm6ZWuJnGC1rXQZ1018M&index=20)

- **Network Configuration in Ubuntu Using Netplan**
    - Ubuntu **no longer uses** `/etc/network/interfaces` for network configuration.
    - Instead, it relies on **Netplan**, with files stored in `/etc/netplan/`.
    - Netplan configurations are **YAML-based** and require precise indentation.
- **Finding and Editing Netplan Files**
    - `ls /etc/netplan/` lists available Netplan configuration files.
    - The default file is typically named `01-network-manager-all.yaml`.
    - Edit the file using `sudo nano /etc/netplan/<filename>.yaml`.
- **Setting a Static IP Address**
    - Under `ethernets:`, specify the network interface (e.g., `ens18`).
    - Define `addresses:` with the **desired IP address and subnet** (e.g., `192.168.118.2/24`).
    - Indentation is crucial; incorrect spacing **breaks the configuration**.
- **Applying Network Changes**
    - Use `sudo netplan apply` to apply the new configuration.
    - `ip a` verifies if the **new IP address is assigned**.
    - Syntax errors in the Netplan file can **prevent changes from taking effect**.
- **Differences from Other Linux Systems**
    - Ubuntu’s Netplan is different from Kali’s `/etc/network/interfaces`.
    - CentOS uses **`ifcfg-eth0` files** instead of Netplan.
	- Learning distribution-specific networking tools **improves troubleshooting skills**.


---
#### Next in Playlist: [[21 Testing Connectivity with Ping]]
# Video 17
![](https://www.youtube.com/watch?v=CfLYrLpsUsQ&list=PLqux0fXsj7x3WYm6ZWuJnGC1rXQZ1018M&index=17)

- **Understanding Network Configuration**  
	- Networking is a **fundamental service** for system communication.  
	- Different **Linux distributions handle networking differently**.  
	- Learning **basic networking concepts** is essential for troubleshooting.  
- **Checking Network Interfaces**  
	- `ifconfig` was a **traditional** command but is now deprecated in Ubuntu.  
	- `ip a` (or `ip addr show`) is the **modern replacement**.  
	- Displays **all active network interfaces** and their IP addresses.  
- **Loopback vs. Ethernet Interfaces**  
	- `lo` (loopback) is for **internal communication** (`127.0.0.1`).  
	- Ethernet interfaces (`eth0`, `ens18`) connect to **external networks**.  
	- Not all interfaces **have an assigned IP address** by default.  
- **Differences Between Distributions**  
	- Ubuntu **uses `ens18`** instead of `eth0` for Ethernet.  
	- Kali **supports `ifconfig`** but also works with `ip a`.  
	- CentOS **can have multiple interfaces** (e.g., `eth0`, `eth1`) for routing.  
- **Configuring Network Interfaces**  
	- Some systems **automatically assign an IP address**, others require manual setup.  
	- Understanding interface **naming conventions** prevents command failures.  
	- Routers require **multiple interfaces** to connect different networks.  
- **Practical Use Cases**  
	- Running `ip a` helps **verify network status**.  
	- Identifying **active interfaces** prevents configuration mistakes.  
	- Knowing the **correct interface name** is crucial for applying settings.  


---
#### Next in Playlist: [[18 Static Configuration in Kali with Interfaces File]]
Video 38

- snmp?

## Tools

### `netstat`
Lists out network connection statistics

- `netstat -tu` -> filter only connections to tcp and udp 
	- -tun -> resolve names to corresponding port
	- -tuna -> also print out listening connections
	- -tunap -> also get process ids (PID) for each connection process. requires sudo
- `netstat | grep ESTABLISHED`

### `ss`
Similar to `netstat`. Alternative

### `kill`
Kill malicious processes / red team connections!

- `kill <pid>`
- 

### `pkill`
Similar to `kill`, allowing for more specific targets.
- killing by userid/name, etc...
- Don't accidentally kill your own/team's sessions!

### `w`
Shows who is logged in and from where

### `top` / `htop`
A lot like task manager, but in the CLI


### `ps`
Search active processes. Nuanced options


## Communication with users / teammates!

### `wall`
"Broadcasts" a message to all users
- `wall "Server shutting down in 5 minutes. Please save your work.`

### `write`
Send basic DMs to a target user.
- `sudo write bob pts/2`

## Red Flags
- random scripts running in the background
- new malicious cronjobs


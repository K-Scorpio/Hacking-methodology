# Active Reconnaissance

* My go to scan is `nmap -sC -sV -oA nmap/<filename> <IP_Address>`. This command will only scan the 1000 most common ports.

	Example: 

```
nmap -sC -sV -oA nmap/Windows_Server_2019 10.10.10.10 
```

> I use the `-oA` to save the scan results in multiple formats, that way I can always go back to it without needing to re-run the scan. It also reduces network activity and you can export the results in other tools.

* It is always good to run a full scan just in case we miss something with the first one. We use the `-p-` for that, this will scan all 65535 ports.
	
	Eample: 

```
nmap -sC -sV -p- -oA nmap/Windows_Server_2019 10.10.10.10
```

* By default nmap performs TCP scans. So we should also perform UPD scans just to be thorough. Keep in mind that those are significantly slower and they require root privileges, so use `-vv` to keep track of what's happening.
	Example: 

```
sudo nmap -sU --top-ports 1000 -sC -sV -vv 10.10.10.10
```
OR 

```
sudo nmap -sU -p- -sC -sV -vv 10.10.10.10
```




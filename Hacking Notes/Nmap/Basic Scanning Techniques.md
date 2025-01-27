Using just Nmap [ip] can work sometimes but a lot of the times the target will block the probes so it will report down.

When you do get a report back it will list the available ports

Port                     State               Service

Ports that respond to the scan be classified as one of the following 6 : open, closed, filtered, unfiltered, open | filtered, closed | filtered

Nmap is also able to scan multiple targets at once 

nmap [range of IPS]

you can also scan the CID, just use the 

ip addr show on linux 

use --> nmap -sn CIDR to ping scan all devices

-6 is used to scan the ipv6 of the target 

nmap -Pn ip is really good 

use arp-scan --localnetwork


1
77
1
154
169
194
203
254
220
230

- `sudo nmap -sV -O -n 192.168.X.X/24`
    
    - Replace `192.168.X.X/24` with your network range (e.g., `192.168.1.0/24`).
    - **Explanation**:
        - `-sV`: Detects service versions.
        - `-O`: Attempts to identify the operating system.
        - `-n`: Skips DNS resolution to speed up the scan.
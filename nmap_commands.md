Nmap Commands:

1. Scan a System with Hostname and IP Address

[root@server1 ~]# nmap server2.tecmint.com

[root@server1 ~]# nmap 192.168.0.101

2. Scan using “-v” option
“-v” option gives more detailed information about the remote machine.
[root@server1 ~]# nmap -v server2.tecmint.com

3. Scan Multiple Hosts
[root@server1 ~]# nmap 192.168.0.101 192.168.0.102 192.168.0.103

4. Scan a whole Subnet
[root@server1 ~]# nmap 192.168.0.*

5. Scan Multiple Servers using last octet of IP address
[root@server1 ~]# nmap 192.168.0.101,102,103

6. Scan list of Hosts from a File
[root@server1 ~]# nmap -iL targets.txt

7. Scan an IP Address Range
[root@server1 ~]# nmap 192.168.0.101-110

8. Scan Network Excluding Remote Hosts
[root@server1 ~]# nmap 192.168.0.* --exclude 192.168.0.100


9. Scan OS information and Traceroute
[root@server1 ~]# nmap -A 192.168.0.101

10. Enable OS Detection with Nmap
Use the option “-O” and “-osscan-guess” also helps to discover OS information
[root@server1 ~]# nmap -O server2.tecmint.com

11. Scan a Host to Detect Firewall
The below command will perform a scan on a remote host to detect if any packet filters or Firewall is used by host.
[root@server1 ~]# nmap -sA 192.168.0.101

12. Scan a Host to check its protected by Firewall
To scan a host if it is protected by any packet filtering software or Firewalls.
[root@server1 ~]# nmap -PN 192.168.0.101

13. Find out Live hosts in a Network
With the help of “-sP” option we can simply check which hosts are live and up in Network, with this option nmap skips port detection and other things.
[root@server1 ~]# nmap -sP 192.168.0.*


14. Perform a Fast Scan
You can perform a fast scan with “-F” option to scans for the ports listed in the nmap-services files and leaves all other ports.
[root@server1 ~]# nmap -F 192.168.0.101

15. Find Nmap version
You can find out Nmap version you are running on your machine with “-V” option.
[root@server1 ~]# nmap -V
[root@server1 ~]# nmap --version

16. Scan Ports Consecutively
Use the “-r” flag to don’t randomize.
[root@server1 ~]# nmap -r 192.168.0.101

17. Print Host interfaces and Routes
You can find out host interface and route information with nmap by using “–iflist” option.
[root@server1 ~]# nmap --iflist

18. Scan for specific Port
There are various options to discover ports on remote machine with Nmap. You can specify the port you want nmap to scan with “-p” option, by default nmap scans only TCP ports.
[root@server1 ~]# nmap -p 80 server2.tecmint.com

19. Scan a TCP Port
You can also specify specific port types and numbers with nmap to scan.
[root@server1 ~]# nmap -p T:8888,80 server2.tecmint.com

20. Scan a UDP Port
[root@server1 ~]# nmap -sU 53 server2.tecmint.com

21. Scan Multiple Ports
You can also scan multiple ports using option “-p“.
[root@server1 ~]# nmap -p 80,443 192.168.0.101

22. Scan Ports by Network Range
You can scan ports with ranges using expressions.
[root@server1 ~]#  nmap -p 80-160 192.168.0.101

23. Find Host Services version Numbers
We can find out service’s versions which are running on remote hosts with “-sV” option.
[root@server1 ~]# nmap -sV 192.168.0.101

24. Scan remote hosts using TCP ACK (PA) and TCP Syn (PS)
Sometimes packet filtering firewalls blocks standard ICMP ping requests, in that case, we can use TCP ACK and TCP Syn methods to scan remote hosts.
[root@server1 ~]# nmap -PS 192.168.0.101

25. Scan Remote host for specific ports with TCP ACK
[root@server1 ~]# nmap -PA -p 22,80 192.168.0.101

26. Scan Remote host for specific ports with TCP Syn
[root@server1 ~]# nmap -PS -p 22,80 192.168.0.101

27. Perform a stealthy Scan
[root@server1 ~]# nmap -sS 192.168.0.101


28. Check most commonly used Ports with TCP Syn
[root@server1 ~]# nmap -sT 192.168.0.101

29. Perform a tcp null scan to fool a firewall
[root@server1 ~]# nmap -sN 192.168.0.101

30. Display the reason a port is in a particular state:
[root@server1 ~]# nmap --reason 192.168.1.1
[root@server1 ~]# nmap --reason server1.gbhackers.com

31. Show all packets sent and received:
[root@server1 ~]# nmap --packet-trace 192.168.1.1

32. Only show open (or possibly open) ports:
[root@server1 ~]# nmap --open 192.168.1.1

33. Scan top ports i.e. scan $number most common ports ##
[root@server1 ~]# nmap --top-ports 5 192.168.1.1
[root@server1 ~]# nmap --top-ports 10 192.168.1.1
 

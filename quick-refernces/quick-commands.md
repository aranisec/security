&lt;!--  
 /\* Font Definitions \*/  
 @font-face  
	{font-family:"Cambria Math";  
	panose-1:2 4 5 3 5 4 6 3 2 4;  
	mso-font-charset:1;  
	mso-generic-font-family:roman;  
	mso-font-pitch:variable;  
	mso-font-signature:0 0 0 0 0 0;}  
 /\* Style Definitions \*/  
 p.MsoNormal, li.MsoNormal, div.MsoNormal  
	{mso-style-unhide:no;  
	mso-style-qformat:yes;  
	mso-style-parent:"";  
	margin:0cm;  
	margin-bottom:.0001pt;  
	mso-pagination:widow-orphan;  
	font-size:10.0pt;  
	font-family:"Times New Roman",serif;  
	mso-fareast-font-family:"Times New Roman";}  
.MsoChpDefault  
	{mso-style-type:export-only;  
	mso-default-props:yes;  
	font-size:10.0pt;  
	mso-ansi-font-size:10.0pt;  
	mso-bidi-font-size:10.0pt;}  
@page WordSection1  
	{size:612.0pt 792.0pt;  
	margin:72.0pt 72.0pt 72.0pt 72.0pt;  
	mso-header-margin:36.0pt;  
	mso-footer-margin:36.0pt;  
	mso-paper-source:0;}  
div.WordSection1  
	{page:WordSection1;}  
--&gt;  


**RECON AND ENUMERATION**

| **Command** | **Description** |
| :--- | :--- |
| nmap -T4 -A -Pn -oA scan -v 192.168.1.1-254 | Full scan |
| for i in 21 22 23 80 443 445;do cat scan.gnmap\|grep " $i/open"\|cut -d "" -f2 &gt; $i.txt;done | Parse results into txt files per port |
| nmap -T4 -v -oA myshares --script smb-enum-shares --script-args smbuser=pwndizzle,smbpass=mypassword -p445 192.168.1.1-254 | Check for open shares |
| dig axfr[example.com](http://example.com/)@[ns1.example.com](http://ns1.example.com/) | DNS zone transfer \(Linux\) |
| tcp.port, tcp.srcport, ip.src, ip.dst, or, and | Wireshark syntax |
| tcpdump tcp port 80 -w output.pcap -i eth0 | Tcpdump syntax |
| mount 192.168.1.1:/share /mnt/nfs | Mount an NFS share |
| mount -o nolock -t nfs -o proto=tcp,port=2049 172.16.1.1:/ /mnt | Mount an NFS share |
| mount -t cifs -o username=&lt;user&gt;,password=&lt;password&gt;,domain=[example.com](http://example.com/)//WIN\_PC\_IP/&lt;share name&gt; /mnt/windows | Mount a Windows share |
| net use x: \\filesvr001\folder1 &lt;password&gt; /user:domain01\jsmith /savecred /p:no | Mount a Windows share |
| net use \\&lt;target&gt;\IPC$ "" /u:"" | Null session |
| rpcclient -U ""&lt;target&gt; | Null session |
| [enum4linux.pl](http://enum4linux.pl/)192.168.1.20 | Retrieve domain info |
| onesixtyone -c names -i snmphosts | SNMP enum |
| snmpcheck -t 172.10.1.1 -c public | SNMP enum |
| nslookup -&gt; set type=any -&gt; ls -d &lt;domain&gt; | DNS zone transfer \(Windows\) |
| nmap --script=smb-check-vulns --script-args=unsafe=1 -p445 &lt;host&gt; | SMB vuln scan |

  
  





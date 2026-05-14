# ARP-Attack-and-Network-Sniffing
# Explore Network Sniffing and ARP Attacks

# AIM:

To explore network sniffing and ARP Attacks

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## ARP Attacks:  
ARP spoofing: A hacker sends fake ARP packets that link an attacker's MAC address with an IP of a computer already on the LAN. 
Boot kali and Windows7 virtual machines.
In windows 7 give the command arp -a
## OUTPUT:

<img width="752" height="536" alt="Screenshot 2026-05-14 093728" src="https://github.com/user-attachments/assets/952f2e02-0535-402b-aeaf-0d2c5b32e2ce" />

Purpose:

Displays the ARP (Address Resolution Protocol) table/cache of your machine.

What ARP table contains:

Mapping between:
IP Address → MAC Address

From kali linux issue the command :
sudo arpspoof -i eth0 -t <target system> <gateway>

Explanation part by part:

sudo
Runs the command with administrator (root) privileges.
Needed because network packet manipulation requires elevated permissions.
arpspoof
A tool used to send fake ARP (Address Resolution Protocol) messages on a local network.
Commonly used in authorized network security labs to demonstrate ARP poisoning / man-in-the-middle concepts.
-i eth0
-i means interface.
eth0 is the network interface (network adapter) being used.
So the attack packets are sent through eth0.
-t <target_ip>
-t means target.
Specifies the victim machine’s IP address.
<gateway_ip>
Usually the router/default gateway IP.
The command tells the victim that the attacker’s MAC address belongs to this gateway IP.
## OUTPUT:


 dsniff:

<img width="1920" height="1043" alt="ss001" src="https://github.com/user-attachments/assets/d422bf09-5e75-4a09-baa9-da233eafedbd" />



Meaning:

dsniff is a network packet sniffing tool.

Purpose:

Captures and analyzes network traffic on a local network.
Commonly used in authorized security labs to observe unencrypted traffic.

What it can do:

Monitor packets passing through the network
Extract readable data from insecure protocols such as:
HTTP
FTP
Telnet
POP3
IMAP

Example:
If a machine sends plain-text login credentials over HTTP/FTP, dsniff may display that data because it is unencrypted.


In Metasploit open the ftp console as below. Also you can try other ftp websites ftp.vim.org
## OUTPUT:
<img width="614" height="435" alt="Screenshot 2026-05-12 203632" src="https://github.com/user-attachments/assets/9de302b4-a68b-436b-9544-2d7d7e840c4c" />




In Kali issue the following commands:
sudo dsnifff
## OUTPUT:
<img width="1920" height="1043" alt="ss001" src="https://github.com/user-attachments/assets/e73eef80-bbbd-4af4-8626-9b48d8054e0d" />


Explanation:

sudo
Runs the command with administrator/root privileges.
Needed because capturing network packets requires elevated permissions.
dsniff
Starts the packet sniffing tool.
Listens to network traffic and tries to extract readable information from unencrypted protocols.

What happens:

The tool begins monitoring packets on the default network interface (or a specified one if you use -i).
It may display information such as:
HTTP data
FTP usernames/passwords
Telnet sessions
Other plain-text network traffic

Invoke the wireshark and examine the various menus  and controls of the tool:
<img width="920" height="1030" alt="image" src="https://github.com/user-attachments/assets/69455035-c734-41a8-bca6-4b74b11a0d6d" />




# ARP SPOOFING



<img width="1920" height="1043" alt="ss1" src="https://github.com/user-attachments/assets/fd25c397-b52b-4559-b848-ab2c5cb6e4a8" />
<img width="1920" height="1043" alt="ss2" src="https://github.com/user-attachments/assets/6b9dc9e8-2c6a-4406-8323-fda50f27b8eb" />

<img width="1920" height="1043" alt="lab4eth" src="https://github.com/user-attachments/assets/94dddd10-0577-4630-b39a-a64c57cea3a3" />







## RESULT:
The kali linux tools for ARP Attack and Network Sniffing were identified successfully

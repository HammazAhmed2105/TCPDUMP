# TCPDUMP
<h2>Lab Summary</h2>
The TCPDump lab on Kali Linux focuses on teaching users how to capture packets using the command-line tool TCPDump. The objective is to familiarize individuals with packet capturing, without the need for a graphical user interface like Wireshark. The lab covers essential tasks and commands, providing a comprehensive walkthrough.
<h2>Lab Objective </h2>
Learn to capture packets using tcpdump.
<h2>Lab Tool</h2>
Kali Linux
<h2>TASK 1</h2>
<b>TCPDUMP is already installed in kali linux by default. First we use the command “tcpdump –version” and then tcpdump –help. Respectively with each command we get to know the version of tcpdump we are running and the available commands we can use.</b>
<img src="https://i.imgur.com/J8lf6Sh.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<b>In order to start the packet capture we need to first select an interface. In simpler words interface can be your wifi or ethernet connection. Type the command “tcpdump -D”</b>
<img src="https://i.imgur.com/QOMlweq.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<b>We can slelect the eth0 interface by using the command “tcpdump -I eth0”, furthermore we can add -c 5 to the command which will hence capture only 5 packets. So the final command would be tcpdump -I eth0 -c 5. (Use the command in root)</b>
<img src="https://i.imgur.com/PYCSBrq.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<b> In case youre interested in adding the MAC Adresses as well, then add the -e to the above command. That is tcpdump -e -I eth0 -c 5</b>
<img src="https://i.imgur.com/5P5t4iu.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<h2>TASK 2</h2>
<b>Using the verbose option in the command for packet capture is recommended since it provides us with extra data integrity information like Time to Live, total length, etc. All we need to do is add a -v parameter. Below you can see the difference between both commands. The above one uses a verbose option and the down one doesn’t. </b>
<img src="https://i.imgur.com/yH9K2XP.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<b>Some other commands can be :
tcpdump -n “udp and dst port 53” This command will help you pickup DNS Requests.</b>
<b>Tcpdump port 443 This command can help capture packets only related to port 443. Replace 443 with anyport number you want.</b>
<b>There are tons of other ways to use the tcpdump. Here a link to help you out. https://docs.netgate.com/pfsense/en/latest/diagnostics/packetcapture/tcpdump.html</b>

<h2>TASK 3</h2>
<b>To print each packet in ASCII code, we need to use “-A” parameter. This next command is an example of using grep with tcpdump to help it only display information we deem to be important. 
•	tcpdump -n -i eth0 -A | grep -e “POST”</b>
<b>This command will begin gathering all packets using tcpdump, and we then use grep to find and display all POST requests to us. This is an example of how tcpdump can be used in a creative fashion to display detailed information about the network.</b>
<img src="https://i.imgur.com/zm0Xx6S.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<h2>TASK 4</h2>
<b>We can save our captured file as well. We need to add a -w and a filename with the extension .pcap at the end</b>
<b>Tcpdump  -I eth0 -c 5 -w sess.pcap</b>

<img src="https://i.imgur.com/4k3837r.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>




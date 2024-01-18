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

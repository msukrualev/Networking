Network 
Hands-on Lab

29th December 2022

The basic network commands in Windows/Linux will be practised in this hands-on exercise.
For the network infrastructure and subnetting demonstration, AWS services will be used.


# Create A Logical Network in the Cloud

Show creating a VPC as a sample for LAN
- indicate IP range
- indicate subnets
- indicate routing tables
- indicate security groups

# Use Windows Firewall

Inbound
Outbound rules


# Use Networking Commands

Use VsCode 
- use git bash (Windows)
- use vsCode or Mac terminal

- use ipconfig or ifconfig to find out your local private ip


- use ping
- test if your network is connected to the internet
ping google.com 
- test if your gateway and connected hosts respond to ping
ping 192.168.1.1

- use traceroute
shows possible routes accross the network
used to troubleshoot if a router fails to work properly
tracert
traceroute

traceroute -n google.com


- use telnet
if a server responds to ping or tracert/traceroute it does not mean that is is fully operational.
for instance there is a web server on thet machine that responds to pings, or it may not respond to pings if the ICMP port is closed. however the web service should be up and running. To check if it is up and running we may use telnet and port as parameter

telnet serverIP 80
telnet google.com 443


- use curl
curl is an open-source data transfer tool
you can get an entire web page or download a file
curl google.com
curl -O google.com/doodles/childrens-day-2014-multiple-countries

if curl results error codes than 
because there is no transmission on port 80


HTTP Response Codes

Code	What It’s Telling	What it Means
200	OK	Request succeeded.
302, 307	Found, Temporary Redirect	The URI of the requested resource has been changed temporarily.
301, 308	Moved Permanently, Permanent Redirect	The URI of the requested resource has been changed permanently.
400	Bad Request	The server can’t understand the request being sent.
401	Unauthorized	The client must authenticate itself before sending the request.
403	Forbidden	The client does not have enough permission to access the content.
404	Not Found	The server can’t find the requested resource.
408	Request Timeout	The response was sent to an idle connection and the server wants to terminate it.
418	I am a Teapot	The server refuses to brew coffee because it is, permanently, a teapot.
500	Internal Server Error	The server does not know how to handle a request.
502	Bad Gateway	The server you are trying to access is a gateway or a reverse proxy (it sits between the client and an actual server that serves the page). You get this error when the gateway gets an incorrect response from a source server.
503	Service Unavailable	The server can’t process the request. This usually happens when a server is down or overloaded.
504	Gateway timeout	Similar to 502, the gateway can’t get a response in time.


- use host
host public-IP-of-server
gives the domain

host google.com
gives the IP addresses

- use Domain Information Groper
dig google.com


- use wget to download a file or a web page
wget google.com
wget google.com/doodles/new-years-day-2012


- use netstat for network statistics
Netstat shows active TCP connections as well as ports on which the server is listening.
netstat


view ports
netstat -s

view routes
netstat -r

- use ssh for secure remote connections
ssh [user_name@ipaddress]

- use scp for secure copying of files
scp [file] [user_name@ipaddress:/foler/file]


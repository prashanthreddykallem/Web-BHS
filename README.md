# Steps that take place when you load a webpage

## Step 1 Enter www.xoken.org
Enter the address in the address bar of the web browser 

## Step 2 DNS Search 

**Domain Naming System** is a naming system which assigns human understandable names to the addresses (IP address ) of servers . It is used to translate domain names (Human understandable) to IP addresses.

When you enter a Domain Name (www.xoken.org) the browser initiates the DNS lookup.It first check the cache(Browser,OS,router,ISP) to find the IP address of the required server.
If the address is not found in the cache then it is looked up in multiple DNS servers on the Internet until we find the address 


## Step 3 TCP Connection 
**Transmission Control Protocol** is the most common protocol used on the internet for connections. It is connection oriented,reliable protocol

Once we get the IP address of www.xoken.org (144.217.163.51) we establish a TCP connection between the client and the server   
TCP Connection is established using three way handshake
This is a three step process where the client and the server exchange SYN (synchronize) and ACK (acknowledge) messages to establish the connection

1. Client sends an SYN packet to Server to check if the Server is read for new connections with a sequence number n  
2. The Server responds by sending a SYN-ACK packet the sequence number is set to n+1 and another sequence number (choosen by server) m
3. The Client will receive the SYN-ACK packet and respond with ACK the seqeunce numbers are set to n+1 and m+1   

With this a connection is established between Client and the Server

## Step 4 HTTP  

**Hyper Text Transfer Protocol** is a protocol used for transfer of hypertext . It is used to for sending and receiving data between client and server

The Client sends a HTTP request message to the server.The request may be of the form GET or POST
The browser send a GET request to the xoken server.
The server has a web server (Apache/2.2.22 (Debian)).It receives the request from the browser and passes it to a request handler to read and generate a response
The request handler is written in server side languages like PHP,ASP.NET,Ruby etc
It generates the response in a certain format like HTML,CSS,XML,JSON etc
This response along with HTTP Response header is sent to the client 

## Step 5 Display of Web page 
The browser will load the HTML web page and if there are any HTML tags like <img> it will send a request to load that element


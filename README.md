Download Link: https://assignmentchef.com/product/solved-csc361-program-1-http-and-web-server-lab
<br>
In this lab, you will learn the basics of socket programming using TCP connections in Python:

how to create a TCP socket, how to bind it to a specific address and port, how to send and receive an HTTP packet.

You need to implement a simple client that sends an HTTP request at a time. You also need to develop a web server that handles the HTTP request.

Your web server should accept and parse the HTTP request, get the requested file from the server’s file system, create an HTTP response message, and then send the response directly to the client. More specifically, if the requested file is present in the server’s file system, your web server should send an HTTP/1.1 200 OK <strong>AND</strong> the content of the requested file to the client; if the requested file is not present in the server’s file system, the server should send an HTTP 404 Not Found message back to the client.

Your client should display <strong>ALL</strong> the messages received from the web server. In particular, your client should display all the content of the requested file if it is present in the server’s file system.

You are provided is a skeleton code for the Web server. You are required to complete the skeleton code server.py . The places where you need to fill in code are marked with

??????????? . Each place may require one or more lines of code. However, you need to develop your client code from scratch. (<strong>Note:</strong> You may modify server.py any way you like, as long as it meets the above requirements. You may even ignore this sample code and start all over from scratch.)

You will also need some basics of HTTP header format in this programming assignment.

<h1>Run the Server/Client inside CSC361-VM</h1>

Within CSC361-VM, open a terminal and type sudo mn -x to create a simple network topology (more details about the created topology can be found in <a href="http://mininet.org/walkthrough/#part-1-everyday-mininet-usage">Mininet Walkthrou</a><a href="http://mininet.org/walkthrough/#part-1-everyday-mininet-usage">g</a><a href="http://mininet.org/walkthrough/#part-1-everyday-mininet-usage">h</a><a href="http://mininet.org/walkthrough/#part-1-everyday-mininet-usage">)</a>. Then pick h1 and h2 to run your server/client code, and start Wireshark to capture packets. Note that you should not open the Wireshark before sudo mn -x command.

<h2>How to Run the Server</h2>

Determine the IP address of the host that is running the server (e.g., the IP address of host h1). Then run a working version of your server program server_web.py . Note that you should run your server first. The following is an input command format to run the server.

For example, if your server is running over IP address A.B.C.D and port number 6789, then the command format can be

<h2>How to Run the Client</h2>

Your client will connect to the server using a TCP connection, send an HTTP request to the server, and display the server response as an output. You can assume that the HTTP request sent is a GET method. The client should take command line arguments specifying the server IP address or host name, the port at which the server is listening, and the path at which the requested object is stored at the server. The following is an input command format to run the client.



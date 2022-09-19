# Systems-Lab-Project-
Base64 Encoding System
Implemented a chat application with Base64 encoding system for client and server to communicate with each other
based on TCP sockets.Server is concurrent and accepts connections from multiple clients and serves all of them concurrently

Initially, server will be waiting for a TCP connection from the client. Then, client will connect to the server using 
server’s TCP port already known to the client. After successful connection, the client accepts the text input from
the user and encodes the input using Base64 encoding system. Once encoded message is computed the client
sends the Message (Type 1 message) to the server via TCP port. After receiving the Message, server should
print the received and original message by decoding the received message, and sends an ACK (Type 2 message)
to the client. The client and server should remain in a loop to communicate any number of messages. Once the
client wants to close the communication, it should send a Message (Type 3 Message) to the server and the TCP
connection on both the server and client should be closed gracefully by releasing the socket resource.

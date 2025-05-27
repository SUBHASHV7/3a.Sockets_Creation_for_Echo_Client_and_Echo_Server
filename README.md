# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.

**Developed by: Subhash V** 

**Register no: 212224240163** 

## PROGRAM

**SERVER:**
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
**CLIENT:**
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```

## OUPUT

SERVER:

![439506819-52f6bc0a-b2dc-4cd6-abe1-843c98c43a05](https://github.com/user-attachments/assets/6e2e6e7d-aa37-40a0-b26d-1bef067325d9)

CLIENT:

![439506837-d2621874-2eea-40b0-a896-28c4fcc16903](https://github.com/user-attachments/assets/0c911cd5-0710-4dd0-a328-7ec77eb29077)

## RESULT

Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

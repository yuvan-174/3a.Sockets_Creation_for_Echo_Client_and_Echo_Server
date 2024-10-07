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
## PROGRAM
## CLIENT:
```py
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())  
```
## SERVER:
```py
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode()) 
```
## OUPUT
## CLIENT:
![Screenshot 2024-10-07 135011](https://github.com/user-attachments/assets/02e3ce8b-bc2d-4795-826a-8e676579052f)

## SERVER:
![Screenshot 2024-10-07 1350112](https://github.com/user-attachments/assets/4f59ef23-569e-41a2-a37a-abf816aa3fe9)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

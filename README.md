# 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME: K GOUTHAM
## REGISTER NUMBER: 212223110019
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT:
```PY
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```
## SERVER:
```PY
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
   ClientMessage=c.recv(1024).decode()
   print("Client > ",ClientMessage)
   msg=input("Server > ")
   c.send(msg.encode())
```
## OUTPUT
### CLIENT:
![image](https://github.com/user-attachments/assets/0c292b09-6693-4520-a3c6-b019513a0129)
### SERVER
![image](https://github.com/user-attachments/assets/3bb6f72b-69dd-4468-87c5-d26233cffdbe)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

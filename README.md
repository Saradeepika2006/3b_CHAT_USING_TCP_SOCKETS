# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
```
CLIENT:
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
```
SERVER:
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
## OUPUT
![Screenshot 2025-05-10 165634](https://github.com/user-attachments/assets/abc9d023-32f8-4d10-a8ac-8e568a8120a3)
![Screenshot 2025-05-10 165648](https://github.com/user-attachments/assets/1b4e6668-480c-4c11-92b8-84b4e2a8ba58)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

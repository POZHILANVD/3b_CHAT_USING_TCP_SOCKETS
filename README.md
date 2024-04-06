# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server:
```
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
## OUTPUT:
### Client:
![Screenshot 2024-04-06 231252](https://github.com/POZHILANVD/3b_CHAT_USING_TCP_SOCKETS/assets/144870498/3e79c422-cb1d-40b0-93f4-557032b8e4e1)

### Server:
![Screenshot 2024-04-06 231302](https://github.com/POZHILANVD/3b_CHAT_USING_TCP_SOCKETS/assets/144870498/5228da31-68a3-4c76-8008-b9ed28149b1c)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.

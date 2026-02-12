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

server
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
client
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

server

<img width="775" height="172" alt="image" src="https://github.com/user-attachments/assets/d7072ef8-7b0d-4b55-888b-9612939ce31f" />

client

<img width="772" height="140" alt="image" src="https://github.com/user-attachments/assets/4fa02474-a8a6-41b0-a9f3-a8f283c4a535" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

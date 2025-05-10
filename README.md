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
## CILENT
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## SERVER
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
## OUPUT
## CLIENT
![Screenshot 2025-05-10 111025](https://github.com/user-attachments/assets/f6e4ba65-c674-4e74-be9c-891c9343b925)
## SERVER
![Screenshot 2025-05-10 111056](https://github.com/user-attachments/assets/715a3ef1-da93-4dce-ace7-37dcc19474be)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

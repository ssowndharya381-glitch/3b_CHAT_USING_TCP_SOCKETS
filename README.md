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
client.py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
```
server.py
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
<img width="544" height="143" alt="Screenshot 2026-05-15 214508" src="https://github.com/user-attachments/assets/bcee9699-6201-402e-b111-be49bec67a7c" />
<img width="671" height="124" alt="Screenshot 2026-05-15 214457" src="https://github.com/user-attachments/assets/8683552e-d1e4-40c7-a4ab-c379a9f2f064" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

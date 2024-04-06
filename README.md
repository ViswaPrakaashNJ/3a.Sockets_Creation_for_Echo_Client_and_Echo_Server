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
**client.py**
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 

```
**server.py**
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
## OUTPUT
**client.py**

![Screenshot 2024-04-06 102311](https://github.com/ViswaPrakaashNJ/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/150996664/b65757d6-52c9-458f-b47d-788571203326)

**server.py**

![Screenshot 2024-04-06 102248](https://github.com/ViswaPrakaashNJ/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/150996664/8b35386e-0e28-4031-b6a0-2f5927dec49b)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

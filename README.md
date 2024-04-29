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
## PROGRAM:
## client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## server:
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
## OUTPUT:
## client:
![image](https://github.com/Rajaraman77/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/150319383/46da3641-5560-45ef-8ba3-fc9078be1641)
## server:
![image](https://github.com/Rajaraman77/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/150319383/c18d2265-bba7-4025-966b-3de265e3af4e)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

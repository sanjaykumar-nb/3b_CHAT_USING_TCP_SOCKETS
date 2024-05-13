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
## client
```
import socket
s=socket.socket()
s.connect(('localhost',8080))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## server
```
import socket
s=socket.socket()
s.bind(('localhost',8080))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```
## OUPUT
## client
![image](https://github.com/sanjaykumar-nb/3b_CHAT_USING_TCP_SOCKETS/assets/154039979/04cddced-6fe1-45aa-86c2-75edb329eac4)
## server
![image](https://github.com/sanjaykumar-nb/3b_CHAT_USING_TCP_SOCKETS/assets/154039979/0131415e-ecc5-47c9-8881-cfcb9ce1ae33)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

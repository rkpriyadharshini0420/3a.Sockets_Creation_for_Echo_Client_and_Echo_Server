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

**CLIENT**
 ```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())

```
**SERVER**
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

**SERVER**

![cn-ex-3a-server](https://github.com/gururaghav2925/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151489500/866a65a7-7dba-4c9e-9bff-96982902f797)



**CLIENT**

![cn-ex-3a-client](https://github.com/gururaghav2925/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151489500/f04dc0b5-5411-41e1-b1a1-01c4ff8f7ab5)





## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

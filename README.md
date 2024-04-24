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
# client:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())

```
# server:
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
# client:
![Screenshot 2024-03-22 142223](https://github.com/Ashwathm12/3b_CHAT_USING_TCP_SOCKETS/assets/138849225/8db69f1c-cea0-4180-a3bf-280fd6a7f107)

# server:
![Screenshot 2024-03-22 142232](https://github.com/Ashwathm12/3b_CHAT_USING_TCP_SOCKETS/assets/138849225/e2a01b37-efae-4673-9619-d711011ced55)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

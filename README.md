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
```
client side:

import socket

s = socket.socket()
s.connect(('localhost', 8000))

while True:
    msg = input("Client > ")
    s.send(msg.encode())
    print("Server > ", s.recv(1024).decode())

server side:

import socket

s = socket.socket()
s.bind(('localhost', 8000))
s.listen(5)

c, addr = s.accept()

while True:
    clientMessage = c.recv(1024).decode()
    c.send(clientMessage.encode())
```
## OUTPUT

<img width="1920" height="1080" alt="Screenshot (167)" src="https://github.com/user-attachments/assets/58d32883-5d86-4268-ae01-86cd7ead38c2" />
<img width="1920" height="1080" alt="Screenshot (168)" src="https://github.com/user-attachments/assets/bdf2c06d-76d3-4b6e-aee2-9b8949ffea2a" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

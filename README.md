# 3b.CREATION FOR CHAT USING TCP SOCKETS
## REF NO:25015705
### DATE:18-02-2026
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
server.py
~~~
import socket
s=socket.socket()
s.bind(('localhost',10101))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client: ",ClientMessage)
    msg=input("Server: ")
    c.send(msg.encode())
~~~
client.py
~~~
import socket
s=socket.socket()
s.connect(('localhost',10101))
while True:
    msg=input("Client: ")
    s.send(msg.encode())
    print("Server: ",s.recv(1024).decode())
~~~
## OUTPUT
server
<img width="1286" height="1044" alt="Screenshot 2026-02-18 101036" src="https://github.com/user-attachments/assets/8a649a7e-2898-42ec-99ed-d50ccfbe6618" />

client
<img width="1510" height="1044" alt="Screenshot 2026-02-18 101054" src="https://github.com/user-attachments/assets/a1e5d84b-8738-4a56-ae56-0606fa7019a9" />



## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

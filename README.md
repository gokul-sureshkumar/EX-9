# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

DATE :

AIM :

To write a python program for creating Chat using TCP Sockets Links.



ALGORITHM :
```
1.Start the program.
2.Get the frame size from the user.
3.To create the frame based on the user request.
4.To send frames to server from the client side.
5.If your frames reach the server, it will send ACK signal to client otherwise it will sendNACK signal to client.
6.Stop the program.
```
PROGRAM :
## Client:
```python
# Developed By : GOKUL.S
# Register Number : 212222110011
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## Server:
```python
# Developed By : GOKUL.S
# Register Number : 212222110011
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
OUTPUT :
## Client Output:
![image](https://github.com/gokul-sureshkumar/EX-9/assets/121148715/1334cfbc-7b85-4add-9123-5967daeaab30)
## Server Output:
![image](https://github.com/gokul-sureshkumar/EX-9/assets/121148715/6feef7ef-fdc8-4a86-bd42-57eabcfbd624)



RESULT :

Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.



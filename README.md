# 2a_Stop_and_Wait_Protocol
## Name:A.LAHARI
## REG NO:212223230111
## AIM :
To write a python program to perform stop and wait protocol
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM :
# CLIENT:
```
import socket   
s=socket.socket()   
s.bind(('localhost',8000))  
s.listen(5)   
c,addr=s.accept()  
while True:   
i=input("Enter a data: ")   
c.send(i.encode())  
ack=c.recv(1024).decode()   
if ack:   
print(ack)   
continue   
else:   
c.close()  
break   
```

## SERVER:

```
import socket   
s=socket.socket()   
s.connect(('localhost',8000))   
while True:   
print(s.recv(1024).decode())   
s.send("Acknowledgement Recived".encode())   
```
## OUTPUT :

## CLIENT:

![Screenshot 2024-04-10 111908](https://github.com/AnnaLahari/2a_Stop_and_Wait_Protocol/assets/149365425/e0a8a80b-8d6f-4f92-9d30-82c0968e8e1c)


## SERVER:

![Screenshot 2024-04-10 112043](https://github.com/AnnaLahari/2a_Stop_and_Wait_Protocol/assets/149365425/c94a4fff-3556-4b89-b8e2-136b449b32fd)


## RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.

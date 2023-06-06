# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

## DATE:15-03-2023

## AIM :

To write a python program to perform stop and wait protocol

## ALGORITHM :

1.Start the program.

2.Get the frame size from the user

3.To create the frame based on the user request.

4.To send frames to server from the client side.

5.If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client.

6.Stop the program

## PROGRAM :

## CLIENT:
## Developed by : MALARVIZHI G
## Register Number : 212222040096
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
    s.send("Acknowledgement Received".encode())
```
## OUTPUT :
## CLIENT:
![ex02 client output](https://github.com/22008650/EX-2/assets/122548204/97d20c8c-72a5-486c-b5ea-55add1e989cb)
## SERVER:
![ex02 server output](https://github.com/22008650/EX-2/assets/122548204/f1b3e34a-eae5-42a2-b3a2-f96a9d70f9fc)
## RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.



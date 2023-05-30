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

Developed by : MALARVIZHI G


Register Number : 212222040096


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
        
## SERVER:

Developed by :Akash A

Register Number : 212221230003

import socket

s=socket.socket()

s.connect(('localhost',8000))

while True:

    print(s.recv(1024).decode())
    
    s.send("Acknowledgement Received".encode())

OUTPUT :
## CLIENT:
![EX 2 CLIENT](https://github.com/22008650/EX-2/assets/122548204/f694c871-57c6-4913-92f1-e5f12d56e79e)

## SERVER:
![EX 2 SERVER](https://github.com/22008650/EX-2/assets/122548204/7ba3b37c-9cc7-49f2-b5c1-3d619694db5b)



## RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.



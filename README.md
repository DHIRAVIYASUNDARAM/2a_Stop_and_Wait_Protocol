# DHIRAVIYA S
# 212223040041
# 2a_Stop_and_Wait_Protocol
## AIM: 
To write a python program to perform stop and wait protocol
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
# PROGRAM:
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
# SERVER:
```
 import socket
 s=socket.socket()
 s.connect(('localhost',8000))
 while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Received".encode())
```

## OUTPUT:
# CLIENT OUTPUT:
![Screenshot 2024-03-11 210133](https://github.com/DHIRAVIYASUNDARAM/2a_Stop_and_Wait_Protocol/assets/165143880/54c2cd25-cd3e-4f7c-8826-72ec1ee5ddb8)

# SERVER OUTPUT:
![Screenshot 2024-03-11 210152](https://github.com/DHIRAVIYASUNDARAM/2a_Stop_and_Wait_Protocol/assets/165143880/95784f19-d8d8-49f8-9d60-c4dc4405b6bf)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.

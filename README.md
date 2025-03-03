# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
# server code:
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```
# client code:
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'lokesh,3/3/25')
    print(f'Received: {s.recv(1024)!r}')
```
## OUTPUT:
 ![WhatsApp Image 2025-03-03 at 16 42 14_65ef881a](https://github.com/user-attachments/assets/c3bd5772-76e1-4968-b7b2-71ccda92da7f)
![WhatsApp Image 2025-03-03 at 18 34 41_a5ed1855](https://github.com/user-attachments/assets/1f24d764-c7ee-428c-b906-8eca9d4bc255)
 

## RESULT:
The program is executed successfully

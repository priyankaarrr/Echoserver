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
# client
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'priyanka R, 2122223220081')
    print(f'Received: {s.recv(1024)!r}')
```
# server
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
## OUTPUT:
![Screenshot 2025-03-03 083508](https://github.com/user-attachments/assets/a5586a78-e304-4f1d-b842-799c4a4d9224)

## RESULT:
The program is executed successfully.

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
# server.py
```py
# echo-server.py


import socket


HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)


with socket.socket(socket.AF_INE
T, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)

```
# client.py
```py
# echo-client.py


import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, world")
    data = s.recv(1024)


print(f"Received {data!r}")

```

## OUTPUT:

# server_output:

<img width="290" height="129" alt="Screenshot 2026-10-30 134842" src="https://github.com/user-attachments/assets/001634f4-2529-455b-ae84-60e7e71b9ed7" />



# client_output:

<img width="241" height="98" alt="Screenshot 2026-10-30 134855" src="https://github.com/user-attachments/assets/4d9b08a3-74f1-4490-b467-9f745547e360" />







## RESULT:
The program is executed successfully

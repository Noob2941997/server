# server
server_code_by_python
import socket
s = socket.socket()
s.bind((socket.gethostname() , 1234))
s.listen(7)
while True:
     clientsocket,addr = s.accept()
     print ("clint is connected!"+addr)
     clientsocket.send(bytes(input("inter message"),"u tf-8"))

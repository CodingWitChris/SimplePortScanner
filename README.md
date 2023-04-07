# SimplePortScanner
# Put in your Ip addy and make sure you list the ports your want to scan..

import socket 

ip = ''
port_list = ()

for port in port_list:
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    result = s.connect_ex((ip,port)) 

    if result == 0:
        print('_' * 60)
        print('Port: ',port, "Is Open")
        print('_' * 60) 

    else:
        print("Port: ",port,"Is Closed")

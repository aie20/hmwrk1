import socket
import sys
import struct
import time

try:
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    print "Socket successfully created"
except socket.error as err:
    print "socket creation failed with error %s" %(err)


port = 37
TIME1970 = 2208988800L

try:
    host_ip1 = socket.gethostbyname('time-a-g.nist.gov')

except socket.gaierror:

    print "there was an error resolving the host"
    sys.exit()

s.connect((host_ip1, port))

t = s.recv(4)
t = struct.unpack("!I", t)[0]
t = int(t - TIME1970)
s.close()

print "the socket has successfully connected on port == %s" %(host_ip1)
print "server time is", time.ctime(t)
print "local clock is", int(time.time()) - t, "seconds off"
print





try:
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    print "Socket successfully created"
except socket.error as err:
    print "socket creation failed with error %s" %(err)


port = 37
TIME1970 = 2208988800L

try:
    host_ip2 = socket.gethostbyname('time-c-g.nist.gov')

except socket.gaierror:

    print "there was an error resolving the host"
    sys.exit()

s.connect((host_ip2, port))

t = s.recv(4)
t = struct.unpack("!I", t)[0]
t = int(t - TIME1970)
s.close()

print "the socket has successfully connected on port == %s" %(host_ip2)
print "server time is", time.ctime(t)
print "local clock is", int(time.time()) - t, "seconds off"
print

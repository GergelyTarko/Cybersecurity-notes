# SMB
**Port: 139/445**

Server Message Block Protocol (SMB) is a client-server communication protocol used for sharing access to files, printers, serial ports and other resources on a network. 
Servers make file systems and other resources (printers, named pipes, APIs) available to clients on the network. Client computers may have their own hard disks, but they also want access to the shared file systems and printers on the servers.

Clients connect to servers using TCP/IP.

Once they have established a connection, clients can then send commands (SMBs) to the server that allow them to access shares, open files, read and write files, and generally do all the sort of things that you want to do with a file system. However, in the case of SMB, these things are done over the network.


## Enumeration

### enum4linux

Enum4linux is a tool for enumerating information including users, shares, group and member list and more from Windows and Samba systems

[enum4linux guide](tools/enum4linux)

### smbclient

smbclient is a client that can 'talk' to an SMB/CIFS server. It offers an interface similar to that of the ftp program. Operations include things like getting files from the server to the local machine, putting files from the local machine to the server, retrieving directory information from the server, listing shared folders and so on.

[smbclient guide](tools/smbclient)

### lookupsid

Determine what users exist via brute force SID lookups.

Using [impacket](tools/impacket###lookupsid):

`python3 /opt/impacket/examples/lookupsid.py anonymous@target`

Using [Metasploit](tools/Metasploit###lookupsid)

`use auxiliary/scanner/smb/smb_lookupsid`




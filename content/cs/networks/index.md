+++
title = "Networks"
description = "HTTP, DNS, IP, UDP, TCP, security"
+++

Introduction
============

Internet
--------

The *internet* is a network of networks. It is build from interconnected
internet service providers (ISPs) and the end users, called *hosts*.
Between these hosts are *communication links*, such as physical cables
and fibers aswell as radio and satellite transmissions.

#### Packets

Across communication links are *packets*, chunks of data that can be
moved and directed across the internet through *routers* and *switches*.

#### Protocols

A *protocol* is the language at which a message sent across a network
should be interpreted. Protocols define the format of the message, the
order of messages sent and received among network entities, and actions
taken on a message transmission. This message acts as a receipt for the
transmission.

Network Edge
------------

The *network edge* is the set of hosts on the network: *clients* and
*servers*.

#### Network Core

The set of routers that connects the network edges is called the
*network core*. The network edge connects to the network core by local
networks, such as residential networks and institutional networks, or
mobile providers.

#### Digital Subscriber Line

Otherwise known as *DSL*, the *digital subscriber line* is the idea of
using existing telephone line as an access point to internet. The
alternative being to construct more physical connections between hosts
and the network. DSL lines meet at a central office called *DSLAM* where
it is then connected to an ISP.

#### Coax

One can send multiple packets of data across a single communication link
by using varying frequency bands from different signals. This process is
called *frequency division multiplexing*. A common communication link
that uses this technology is called *HFC*, *hybrid fiber coax*, or just
*coax* which is commonly used to stream many television channels across
the same wire. Unlike DSL, coax does not have a central office, which is
why different frequency bands are used.

#### Home Network

Typical home networks use a router that extends from a DSL modem or
cable, which connects directly to hosts or to wireless access points
that in turn connect to hosts wirelessly.

#### Enterprise Access Networks

Larger companies use *ethernet*, which involves connecting ethernet
switches to a router, which then connect hosts to the internet via the
router.

#### Wireless Access Networks

Devices that connect devices wireless to the internet include *wireless
LANs*, which typically service a 100 foot radius, and *wide-area towers*
that can provide service for a radius of many miles.

#### Bandwidth

A message is broken into chucks called packets, composed of a string of
bits. How fast these bits are sent across the network, the link
transmission rate, is called *link bandwidth*.

#### Physical Media

There are various types of physical connections between different hosts.
including *twisted pair*, or *TP*, *coaxial cable*, or *coax*, ahd
*fiber optic cable*. Fiber optic cable in particular is extremely fast
and reliable. In addition, there are types of radio links, such as
*LAN*, *satellite*, and *wide-area*.

Network Core
------------

#### Packet-Switching

The network core is a mech of interconnect routers. The process of
directing packets between the correct host devices is called
*packet-switching*. Before sending a packet, a router must first receive
the entire packet.

#### Routing and Forwarding

The network core has two main jobs. To *route* data, that is, to
determine the optimal way to send the data through the network, and to
*forward*, to actually move the data across the network.

#### How to Connect Access Points

There is an incredible number of access points. What is best way to
connect them? A number of access points will connect to a particular
ISP. Between these ISPs, are *internet exchange points* to allow
connections between providers. On top of all this, are content providers
that are connected to all ISPs.

Packet Loss
-----------

#### Queuing Delay and Loss

When more packets are sent to a router than the router is forwarding,
the router is overloaded and packets back up into memory, called a
*buffer*. Once a threshold is met, packets are simply lost, and the data
never reaches its destination.

#### Sources of Packet Delay

Delay comes from four different sources: nodal processing, queueing
delay, transmission delay, and propagation delay.

#### Buffers

To tackle the delay with queueing, buffers were created to hold data if
the queue is not empty.

Internet Protocol Stack
-----------------------

#### Layering

The internet is a set of layers within a host before taking application
data and sending it across the wire. This methodology is used for a
multitude of reason, one being the opportunity to standardize the
communication between different layers and isolating parts of a local
system for simplicity.

#### The Stack

The five layers are as follows.

1.  *Application*: supports network-accessible applications (FTP, SMTP,
    HTTP)

2.  *Transport*: process-process data transfer (TCP, UDP)

3.  *Network*: routing of datagrams from source to destination (IP,
    routing protocols)

4.  *Link*: data transfer between neighboring network elements
    (ethernet, PPP)

5.  *Physical*: bits on the wire

#### Other Layers Nobody Cares About

They are called *presentation* and *session* layers but we lump these in
with appliation so no worries.

#### Messages Across Layers

Each layer will often add its own header on top of the application layer
message to help direct the message through each layer as it makes its
way back up the stack on the receiving device.

Security
--------

All layers are at risk from malicious use of communications. For
example, there is malware, malicious programs that can be sent over the
internet to a host computer. There are *denial of service* attacks, or
*DoS* which involve overloading a host with packets. There is also
*packet sniffing* which involves capturing packets across the wire and
viewing senstive material.

Application Layer
=================

Network Applications
--------------------

#### Examples

Some network applications include e-mail, streaming video, online
gaming, skype, torrenting, and social networking.

#### Only for Hosts

The application layer is only necessary for hosts. Routers and switches
do not have an application layer.

#### Application Architecture

Two popular structures of network applications are *client-server* and
*peer-to-peer*. In client-server architecture, the server is a host that
is always on with a permanent IP address. It is often structured to
handle scaling as more clients communicate with the server, and not
directly with eachother. Peer-to-peer connects do not use a server, and
require complex management to connect arbitrary end users and to scale
across more users.

#### Processes

A program running on a host is called a *process*. Within the same host,
two processes communicate using *inter-process communication*. All
processes communicate by exchanging *messages*.

#### Necessary Addressing

To receive messages, processes must have an *identifier*, which include
both the IP address and port number associated with the process. An IP
address is a unique 32-bit number which identifies the device. A port
number is a number that identifies which application (on all end users)
the message is sent from and being delivered too.

#### Application Protocol

The appliation layer protocol defines the types of messages exchange
(request or response), the message syntax, the semantics of the message,
and the rules for how to respond and communicate using the message. Some
of the protocols are open which include HTTP and SMTP, while others are
proprietary, like Skype.

#### Requirements for Transport Service

Some apps require 100% reliable data transfer, while others can tolerate
some loss. Some apps needs very low delays to be effective. Some require
a large amount of throughput in a small amount of time, while other work
off whatever throughput they can get. And often apps require encryption
and data security.

#### Internet Protocol Services

Two protocols that applications use are *TCP* and *UDP*.

* _TCP_: Reliable transport, flow control, congenstion control; doesn't
    provide minimal delay guarantee, security.

* _UDP_: Unreliable data transfer; doesn't provide everything else.

Domain Name System
------------------

#### What is it?

The *domain name server* or *DNS* is distributed database of name
servers that connect a name query with an IP address of the web domain.

#### Services

DNS provides hostname to IP address translation, host aliasing, mail
server aliasing, and load distribution.

#### Centralizing DNS

It's a bad idea. Doesn't scale; it's a single point of failure; it would
require the utmost of maintenance.

#### Structure

DNS has diffferent levels of servers. The highest level being *root
servers*, which then communicate with *top-level domain servers* (com,
edu, net), and then communicate with *authoritative name servers*.

#### Communicating Across the Structure

There are two types of queries used across the structure. The first is
called iterated query, where a host communicates with a local DNS server
who then communicates with root DNS server, then TLD server, then
authoriative DNS servers. A recursive query has the host communicate
with a local DNS server who in turn communicates with a root DNS server
who then communicates with a TDL server who then communicates with an
authoritative DNS server.

#### Caching

In order to avoid doing this process too many times for the same record,
hosts will cache the exact name to IP record. This lasts for only a
short amount of time, to enure that if changes happen between the name
and IP that all hosts will see those changes.

#### Resource Records

*Resource records* or *RRs* are distributed database entries that hold
information. They hold *name*, *value*, *type*, and *time to live* or
*ttl*.

#### Type

Each type describes what the name and value mean.

` ` | ` `
---: | ---
        **A**| Name is hostname, value is IP address
       **NS**| Name is domain, value is hostname of authoritative name server for this domain
    **CNAME**| Name is alias for some "canonical" (the real) name, value is canonical name
       **MX**| Value is the name of mailserver associated with name
      **PTR**| Points IP to name
      **TXT**| Anything, often security
      **SOA**| Start of authority
     **AAAA**| Specifies the IPv6 address for a given host.

#### Message Format

Query and reply messages have the same message format. Messages have a
header that has an *identification number* to link queries with replies
and flags that determine if message is a reply or query and if recursion
is desired or is available. Then there is 4 more blocks that include the
number of question, number of answer records, number of authority
records, and number of additional record. Of course this is then
followed by questions, answers, authority, and additional information.

Socket Programming
------------------

#### Sockets

In order for a network application in the application layer to
communicate to the transport layer, messages are passed to a *socket*,
which communicate between the applicastion layer and transport layer.
Sockets communicate using UDP or TCP.

#### Socket Programming with UDP

There is no "connection" between client and server. No "handshaking"
before sending the data. Sender explicitly attached IP destination and
port number to each packet. Transmitted data may also be lost or
received out of order. Data is also sent in *datagrams*, or chucks of
data.

#### An Example of UDP Socket Program

This is an example of using UDP to establish a client-server connection.

* Client: 

```python
from socket import *
serverName = 'hostname'
serverPort = 12000
clientSocket = socket(socket.AF_INET,
        socket.SOCK_DGRAM)
message = raw_input('Input lowercase sentence:')
clientSocket.sendto(message,(serverName, serverPort))
modifiedMessage, serverAddress =
        clientSocket.recvfrom(2048)
print modifiedMessage
clientSocket.close()
```

* Server

```python
from socket import *
serverPort = 12000
serverSocket = socket(AF_INET, SOCK_DGRAM)
serverSocket.bind(('', serverPort))
print "The server is ready to receive"
while 1:
    message, clientAddress = serverSocket.recvfrom(2048)
    modifiedMessage = message.upper()
    serverSocket.sendto(modifiedMessage, clientAddress)
```

#### Socket Programming with TCP

Client must contact the server directly, and the server must have
created a socket that welcomes the client's contact. Once the client
contacts the server using a new socket, the server does the same with
its own socket. Then TCP can communicate using *byte stream transfer*,
or a stream of bits.

#### An Example of UDP Socket Program

This is an example of using TPC to establish a client-server connection.

* Client
```python
from socket import *
serverName = 'servername'
serverPort = 12000
clientSocket = socket(AF_INET, SOCK_STREAM)
clientSocket.connect((serverName,serverPort))
sentence = raw_input('Input lowercase sentence:')
clientSocket.send(sentence)
modifiedSentence = clientSocket.recv(1024)
print 'From Server:', modifiedSentence
clientSocket.close()
```

* Server
```python
from socket import *
serverPort = 12000
serverSocket = socket(AF_INET,SOCK_STREAM)
serverSocket.bind(('',serverPort))
serverSocket.listen(1)
print 'The server is ready to receive'
while 1:
    connectionSocket, addr = serverSocket.accept()
    sentence = connectionSocket.recv(1024)
    capitalizedSentence = sentence.upper()
    connectionSocket.send(capitalizedSentence)
    connectionSocket.close()
```

#### Zones

Zones can be either forward or reverse domains. They transfer domain
requests to other servers.

The Web and HTTP
----------------

#### Overview

Web pages consist of objects, such as an HTML file, pictures, applets,
audio files, etc. Each object is addressable by a URL.

#### Hypertext Transfer Protocol

Also known as *HTTP*, the *hypertext transfer protocol* is the web's
application layer protocol. It follows a client/server model. HTTP uses
TCP to initiated a connection between the client and server. Also note
that HTTP is *stateless*, meaning it maintains no information about past
client requests.

#### Persistent and Non-persistent

Non-persistent HTTP only allows one object to be sent over a TCP
connection at a time, and multiple connections are required to download
more. Persistent HTTP allows multiple objects to be sent in a single
connection.

#### Timing

The amount of time for a packet to travel from the client to the server
and back to the client is called *round trip time* or *RRT*.

#### HTTP Request Message

HTTP requests and responses are in ASCII, human-readable format.
Generally, these messages look like the following.
```
METHOD some.url/path HTTP/1.1\r\n
name: value\r\n
name: value\r\n
...
name: value\r\n
\r\n
body of document until end
```

#### Methods

There are a variety of methods that can be used in the HTTP protocol.

` ` | ` `
--- | ---
       **GET**| Requests for object on domain
      **POST**| Used for sending form input to server
      **HEAD**| Asks server to leave requested object out of response
       **PUT**| Uploads file in entity body to path specified by URL field
    **DELETE**| Deletes file specified in the URL field

#### HTTP Response Message

Generally, these messages look like the following.
```
HTTP/1.1 STATUSNUM STATUSDESC\r\n
name: value\r\n
name: value\r\n
...
name: value\r\n
\r\n
data requested until end
```

#### HTTP Response Status Codes

There are many HTTP response status codes, but here are few.

` ` | ` ` | ` `
  --------------------------------|---------|--------------------------------
                            **OK**| **200** |request succeeded
             **Moved Permanently**| **301** |request object has been moved
                   **Bad Request**| **400** |request message not understood
                     **Not Found**| **404** |request document is not found
    **HTTP Version Not Supported**| **505** |title

#### Cookies

Cookies are a way to store data between client and server, despite HTTP
be stateless. In the HTTP request and response, a cookie is shared in a
header that is stored at the client and used by the server to preserve
information between the connection.

#### Web Proxy

A web proxy is a middle man for client-server interaction. The proxy
server will distribute cached data to clients that access the proxy. If
the requested data is not cached, the proxy will query the server and
cache the requested data.

#### Conditional GET

The client can add a header called 'If-modified-since' which will send
the data if it is new, otherwise will send just a 304 status code to
save on bandwidth between the client and the server, since the cached
data is up to date.

FTP
---

The only thing interesting about the FTP protocol is that it has two
seperate connections, one for data and one for control.

SMTP
----

This protocol is used for distributing email. The only thing interesting
about the SMTP protocol is that it involves a lot of communication back
and forth to communicate a single email.

Transport Layer
===============

Introduction
------------

#### What is it really?

The transport layer provides logical communication between app processes
running on different hosts. Transport protocols only run on end systems,
as only those have an application layer. It is the transport layer that
breaks up packets on the sender side and rejoins packets and the
receiver side.

#### Difference From Network Layer

The network layer is logical connection between hosts, while the
transport layer is logical connection between processes.

#### Internet Transport Layer Protocols

There are two that are most popular. TCP is reliable data transfer, that
includes features like congestion control and flow control at the cost
of overhead. UDP is unreliable and simply an extension of the very
minimal, network layer IP protocol.

#### Multiplexing and Demultiplexing

The first two bytes of a TPC/UDP segment is the source port number,
followed by the destination port number in the second two bytes. From
this, the sender can multiplex the message to the network layer and the
reciever can demultiplex the response.

UDP
---

#### Overview

UDP is a bare-bones protocol to send message across the wire with as
little overhead as possible. In that regard, UDP packets may be lost or
sent out of order. It is also connectionless, meaning there is no
communication between the client and server before data is sent. Data is
simply sent out on the wire with hopes that it will reach its
destination.

#### UDP Segment Format

UDP datagrams have a small header that includes 4 shorts: source port,
destination port, length of entire UDP segment, and checksum. The rest
of the segment is the application layer data, called the *payload*.

#### Perks

Because there is no handshaking, there is no connection delay. It also
had a very small header size, and has no congestion control. This means
that UDP can blast away as fast as desired.

Reliable Data Transfer
----------------------

#### What is it?

The real world, including the physical layer, is subject to change and
is unreliable. Bits can be changes across the medium and packets can be
lost altogether. At the transport layer, the right protocol can similate
a guarunteed correct data transfer for the application layer, despite
that the network layer is inherently unreliable.

#### Problems from Data Transfer and their Solutions

` ` | ` `
--- | ---
           Bit Errors|When a *checksum* fails, the receiver of the lost message sends an *ACK* to tell the sender that the message was recieved.
        Currupted ACK|If an ACK is received and its garbled, then the sender simply resends their message.
    Duplicate Packets|When having to resend a message that the reciever may have already recieved, attached is a *sequence number* so the reciever knows if the packet sent is the same data that was last ACKed. To transmit to the sender which packet was received successully, the ACK also includes the sequence number of the last packet that was received uncorrupted.
         Lost Packets|If the sender never receives an ACK because either the message or the ACK was lost, the sender will resend the packate after a *timeout* as determined by a countdown timer.

#### Stop and Wait Operation

Primitive versions of reliable data transfer send a single packet, and
then wait for an ACK before sending the next packet. But if the round
trip time, or *RRT*, is very long, a large number of packets may take a
very, very long time to send.

#### Pipelining

A piplined protocol is one that sends multiple packets across the
network before expected an ACK for each one.

#### Go-Back-N

In the *go-back-N* pipelining paradigm, the sender sends up to N unacked
packets across the pipeline. The receiver only needs to send a single
cumulative ack. The sender has a timer for the oldest unacked packet.
When it expires, the sender transmits all unacked packets.

#### Selective Repeat

In this pipelining paradigm, the sender sends up to N unacked packets
but also has a timer for each packet because the sender expects an ACK
for every packet sent.

TCP
---

#### Overview

TCP is point-to-point, meaning one sender and one receiver. It is
reliable and in the form of a byte stream. It's pipelined and used full
duplex data, meaning you can have bidirectional data flow in the same
connection. Its connection oriented and flow controlled, as to not
overwhelm the receiver.

#### Segment Structure

-   2-byte source port

-   2-byte destination port

-   4-byte sequence number

-   4-byte acknowledgement number

-   1-byte head length

-   2-bit unused space

-   6 1-bit flags (URG, ACK, PSH, RST, SYN, FIN)

-   2-byte receive window size

-   2-byte checksum

-   2-byte urgent data pointer

-   variable length options block

-   variable length application layer data

The RST, SYN, and FIN flags are used for the beginning handshaking as
well as closing the connection.

#### Timeout

A natural question is to ask how long should the sender wait before
sending again? How long should the countimer be? TCP's implementation
calcalates the timeout as function of the current timeout and the most
recent round trip times. This moving average is then inflated by four
standard deviations.

#### TCP Fast Restransmit

If the sender receives 3 ACKs for the same data, then TCP will resend
unacked segment with the smallest sequence number. Likely the unacked
segment was lost, so TCP does not wait for timeout.

#### Flow Control

The receiver sends back to the sender the size of the congestion window,
which is how many packets the receiver can fit in the remaining space of
the buffer. This guaruntees that the buffer will not overflow.

#### Handshaking

Three way handshakes for the win.

Congestion Control
------------------

Congestion is when the network gets too many packets too quickly and as
a result can't fit all packets in buffers. So these packets are dropped
by the routers which leads to more packets being lost and then resent
across the network. Controlling the rate at which these packets are sent
across the network is called congestion control.

#### Two Paradigms

End-end congestion control is the approach taken by TCP, which involves
no explicit feedback from the network, but is inferred from end-system
observed loss and delay.

#### TCP Congestion Control

TCP starts by sending so many packets, and if all goes successfully, it
will increase its congestion window by 1. It will continue to do this
until there is a loss, at which the congestion window will be cut in
half. How does TCP know a good place to start? TCP has *slow start*
which exponentially increases packets sent from 1 to 2 to 4 to 8 and so
on, until there is a loss. Then it will continue as normal.

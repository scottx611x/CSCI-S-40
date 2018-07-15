## Homework 3
### Scott Ouellette 
### Scott_Ouellette@hms.harvard.edu

#### 1.) 
**Consider an IP network composed of two networks (13.0.0.0/8 and 18.0.0.0/8) connected by a router, R, having interfaces 1 and 2.  The IP addresses of hosts A, B, C, and D, as well as of interfaces R1 and R2, are given in the figure below.  Let the Ethernet address of host A be called MAC_A, of R1 be called MAC_R1, and so forth.**

<img width="469" alt="screen shot 2018-07-15 at 2 57 36 pm" src="https://user-images.githubusercontent.com/5629547/42737283-75eaeee0-883f-11e8-9c0d-8efea4f180ba.png">

**a) Suppose that host A has some application layer data (layer-5) to send to host B using UDP.  Describe this process in detail. Specifically, explain what happens on host A at each of the five layers of the Internet Model. Assume for this question that Host Ahas never sent data before to Host B. Write your answer in the form of a detailed list, such that step 1 in your list is "(1) Host A's application passes its data off to the layer-4 UDP module where it is encapsulated and a UDP header is added."  Be sureto include information on how MAC addresses, IP addresses and subnet masks are used by the host.  Include information on the use of ARP and the use of a routing table (if necessary) in your answer.  Your explanation can stop at the point when A's data reaches B's Ethernet interface; you needn't explain what happens in B's protocol stack.**

**1b) Using the same list format, explain the process by which host A sends some application layer data to host D.  Again, your explanation can stop at the point when A's data reaches D's Ethernet interface. Assume for this question that Host A has never sent data before to the router, or to Host D.PLEASE NOTE: Answering this entire question will probably require two-pages.**

#### 2.) 
**A "tuple" is a term which means "an ordered set of values" and in our readings and discussions we have observed that connections in the Internet can be uniquely identified using a very specific 5-tuple.**

**a.) Describe this specific 5-tuple in detail.**

**b.) Assume that a user working on a laptop has both an email connection and a web connection open simultaneously to a remote server.  Assume that both the laptop and web server are directly connected to the Internet (in other words, they are not behind a NAT device) and that the IP address of the laptop is 128.103.104.105 and that the IP address of the server is 18.19.20.21.  Describe in detail the 5-tuple information that you would find in the connection table of both the laptop and the server.  (As shown in lecture, you would be able to view these details using the Netstat command.)**

#### 3.) 

**a.) Describe the type of information that would be found in a distance vector routing table.  In other words, what are the typical column headings of the routing table in a router using the RIPv2 protocol?**

**b.) Assume that you had to choose either RIPv2 or OSPF as the routing protocol for a large private enterprise network.  Which one would you pick?  Provide three substantive technical reasons for your choice.**

#### 4.) 
**UDP uses a pseudo-header when calculating the checksum of a datagram. (We are referring to the checksum that is included in the UDP header.)  Describe the pseudo-header and how it is used to calculate this checksum.  What potential problem or problems does calculating the checksum in this manner solve?**

#### 5.) 
**TCP includes functionality for both flow control and congestion control. Describe the motivation for each of them. In other words, explain why both are necessary and how do they differ. Alsodescribe how each of them is implemented and works.**

#### 6.)
**a.) Imagine that you are designing a NAT box which used port-mapped network address translation (sometimes known as NAPT.)  As you do your design, you realize that the 5-tuple discussed in class is not sufficient to keep track of the connections which traverse the NAPT box.  It is a good starting point, but the "translation table" in the NAPT box needs additional information.  What information is needed in this table and how is the table structured and managed?  Describe the use of the table in detail.**

**b.) The NAT box you design is implemented and will soon be used to provide IP address sharing for users of cable modems and DSL service.  During the testing though, it becomes obvious that port mapping is not the only capability that is required for a NAT box.  For example, some ICMP diagnostics do not work when the packets are sent through your box.  Explain in detail what is happening, and what changes must be made to the various packet headers by your software so that the packets flow properly across the NAT box.  Given what you have learned, describe any limitations you might expect with your implementation. Be specific.**

#### 7.) 
**a.) What does it mean from a technical standpoint to say that a network supports IPv6?  In other works, what are the critical components and systems that need to be in place for your network to support IPv6.  (This is more than just saying that OSX or Windows 7 supports IPv6.)**

**b.) Determine whether the network you use at work or school supports IPv6, and report your results.  How did you figure this out?  Note that if you work from home and do not use a corporate or campus network then you should determine whether your home network supports IPv6.**
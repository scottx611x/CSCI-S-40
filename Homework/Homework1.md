## Homework 1
### Scott Ouellette 
### Scott_Ouellette@hms.harvard.edu

#### 1.) 
**Imagine that a bicycle messenger is given three (3) USB memory sticks, each of which contains 64
gigabytes of data. Given that the courier can travel at 20 km per hour through traffic, for what range of
distance does the courier have a higher data rate than a transmission line whose data rate (excluding
overhead) is 150 Mbps? Provide the details that support your answer.**

`64 x 3 = 192GB`
`192GB @ 150 mbps ~= 2 Hours and 54 Minutes to transfer over the wire`

The bicycle messenger would therefore be a faster solution for any target within roughly a 60 km radius.

#### 2.) 
**Assume that you are viewing a web page on the course website from a computer located at your home
or your office. Research and describe the network connectivity (referred to as the network topology) and
the network architecture between your computer and the server at Harvard where the web page is located.
If you are not able to get specific information on how your machine is connected to the Internet, describe
how machines in comparable environments would be connected. You can assume for this question that
the web server at Harvard is connected directly to the Harvard backbone network.**

The hops needed to view a webpage from my local network would look something like the following.

My request would travel through my wireless router onward to my cable modem. Then, said request would be handed off to my ISP and go through a couple of hops in the Greater Boston area (due to my proximity to Harvard) while being distributed on the commercial internet. Then once my request makes it along to a place where it can be routed to one of Harvard's Edge routers, it will happen, and then proceed to be directed through Harvard's internal network to the server hosting the afforementioned web page.


#### 3.) 
**Join three different IETF mailing lists of your choice. Tell us which groups you joined. (You receive
3 points for joining the lists.)**

- `Ietf-hub-boston`
- `101-newcomers`
- `Suit -- Software Updates for Internet of Things`


#### 4.) 
**Explain the use of the sliding window for both flow control and error control. Show how the same
sequence numbers that are used for flow control can also be used for error control. Illustrate your answer
using time sequence diagrams.**

Lets draw from the example that Joe talked about in the first section.

Given the sequence numbers `0-7` and a window size of 3, an ideal scenario would be that packets `[0, 1, 2]` get sent out, and the sender recieves an ACK back ensureing that those three were transmitted properly and the window then slides on to `[3, 4, 5]` and so on. 

TCP's implementation of sequence numbers allows for error control to happen based on basic logic. If packets 1, 2, and 4 are recieved its easy to see that packet 3 is missing and a request for retransmission can be sent out.

The sliding window is also useful for flow control in the sense that the it will only accept packets/datagrams for sequence numbers that are in the window at a given time. Otherwise said packets will be discarded dissalowing the sender to overwhelm the reciever.

![img_20180701_231050](https://user-images.githubusercontent.com/5629547/42143682-70ad1d24-7d84-11e8-8489-6d67fe673858.jpg)

#### 5a.) 
**Research the network architecture and technology of cable modems and xDSL service for providing
access to the Internet from your home. Describe in detail the technical features of the transmission and
multiplexing schemes used by each of these services. Your answer should focus on the coax or
twisted pair technology used in these services rather than the use of fiber optics, and your answer
should concentrate on the transmission and multiplexing used by these systems. You will find a lot
of material available on the web to help you answer this question but please note that your answer should
be in your own words, and that your answer should include proper citations.**

One of the most prominent differences with a cable vs dsl connection is that with a DSL connection, your connection to your ISP is your own. This is in contrast to a cable connection where bandwith is shared between users of a given area that connects to the ISP.

DSL also takes a more acute hit in performance degraddation over distance of cabling where a coaxial copper cable wont suffer as much.

Both DSL and Cable are frequency multiplexed aloowing for internet specific traffic to be isolated from other (phone & cable) traffic.

#### 5b.) 
**Spend some time researching new technology that is being developed to provide high-speed Internet
service to residential customers. Describe a new development in this area. (Make sure to provide the
appropriate citations for your answer.) How fast do you expect residential users where you live to be able
to access the Internet two years from today?**

I have done some research and found that there is currently some internet satellites that have been launched recently with a total network capacity of 1 TBPS. See article here: https://www.theverge.com/2016/2/10/10958952/boeing-viasat-fast-internet-developing-countries-rural-homes. The company launching these satellites (ViaSat) make cliams that this new type of satellite will be able to "deliver 100 Mbps service to remote residential properties in the Americas, Europe, the Middle East, Africa, and Asia"

This kind of news isn't only of interest for those residential customers who live in the more remote necks of the woods, but for commercial airlines being able to provide better flight connectivity, as well as being able to "provide 1 Gbps connections to maritime, oceanic and other corporate enterprise applications such as oil and gas platforms."


#### 6a.) 
**What is a virtual circuit? How does it compare to a physical or "real" circuit?**

An example of a physical or real circuit is a dedicated cable with direction connections to said cable (ex. vampire circuits) giving nodes access to information on said cable. A good example of a virtual circuit is: packet switching. There is no actual routing decisions being made on the transfer media (cables). Routing decisions are determined when connections are established.

#### 6b.) 
**Describe, compare and contrast, connection-oriented communication and connectionless
communication. Focus your answer on the protocols at layer 3 (IP) and layer 4 (TCP or UDP).**

TCP and UDP are two examples of connection oriented and connectionless communication, respectively. A connection based layer 4 protocol, TCP in this example, can be based on a connectionless layer 3 protocol (IP), but still can achieve reliable delivery based on segment sequence , "the three step handshake", among other things. A connectionless protocol is implemeted around the lack of a guarantee of no loss coming from a given transfer. There is no state shared between sender and reciever because there is no analog to TCP's segments implemented. This is actually the beauty of connectionless communication, because some error and loss can happen, and a human on the recieving end can generally still digest the result.

#### 6c.) 
**It is very common to hear folks say that connection-oriented communications is the same as circuit
switching or circuit-switched communication. Does this statement make sense? How are the two
concepts and technologies related to each other, and/or how are they different? HINT: Consider the
physical characteristics of a network versus the logical view of the network.**

This statement makes sense to me at first pass. Both circuit switched communication and connection-oriented communication both rely on in-order delivery of streams of data. I think that by definition, this makes circuit-switched communication a connection-oriented communication.



#### 7.) 
**Submit your homework via the course website. Make sure that your name is on your homework
assignment, and also confirm that your last name and the hw# are a part of the file name (as described
above.) We know it seems foolish to mention that you have to put your name on your homework but we
always have a few students that do not do this.**
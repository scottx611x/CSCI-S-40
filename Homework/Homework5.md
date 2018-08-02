## Homework 5
### Scott Ouellette 
### Scott_Ouellette@hms.harvard.edu

#### 1.) CAN-SPAM section 5.a.5 requires all bulk email senders to require an opt-out link on all emails, as well as certain other requirements. How might clicking on these opt-out links be counter- productive for the email recipient?

These opt-out links could potentially sneaky. A given link could indeed opt the recieving user out of getting anymore spam from a given spammer, but the action of clicking on the "opt-out" link could end up signing the receiver up to receive even more spam then before! 

#### 2.) All routers today implement policies for packet filtering and forwarding and most of them use what are called Access Control Lists (ACLs) to configure these policies. Do some research on a commercially available router that uses ACLs (pick the router vendor of your choice) and describe in detail how ACLs are used and how the packet filtering is done. Include specific examples of the ACLs in your answer, but note that you do not need to describe how the hardware implements the packet filtering and forwarding. Make sure to identify the router you are describing. Note that most of the routers meant for home networks do not allow users to configure or view the actual ACLs, rather, they use a simple GUI interface to set router policy; such a device would not be a good example for this question. Also, many of the commercial routers also provide a GUI interface to setting ACLs. For this question it is important that you describe the use of the ACL, not the GUI interface.



#### 3.) What is a X.509 certificate? What is a Certificate Authority? Given that anyone can create a public/private key pair on their own, describe why certificates and certificate authorities are necessary and how they are used?

An X.509 certificate at it's simplist is a culmination of asymmetric cryptography (public/private keys), hashing, and digital signatures. What this certificate is actually providing is a way to verify that a website is trusted. It is a digitally signed doc reflecting a website's identity and public key.

Certificate Authorities are third parties that must be trusted be all actors in a request

CAs are necessary because they prevent a Man in the middle attack from being able to happen


#### 4.) Assume that you are submitting your homework via email. Describe in detail the methodology for using a digital signature using public-key cryptography to sign and submit your homework. (Note that an email that is digitally signed is not the same as encrypting it.)

Encrypt session key with my private key, encrypt again with friends public key. Friend comes along and decrypts with his private key. He then decrypts with my public key to get the session key! He can then go ahead and decrypt the large file.
DomainKeys (DKIM) combat spam emails by digitally signing them with the private key of the sending domain.


#### 5.) Describe the functionality and operation of a SIP proxy server and also the other types of SIP servers that would be used in a network to support VoIP. Try to be clear and specific in your answer about the functionality of each server since current real-world product implementations combine a lot of the functionality into a single box.

Think of the SIP trapezoid! Think of the similarities between SIP PRoxies and MTAs! Important to mention the three phases of the call! Important to mention that the media transfer phase is end-to-end!!!!!!

#### 6.) Assume that you have recently implemented a Layer 2 switching environment in your network that uses OpenFlow. Assume that a packet enters the switch and a lookup is done in the flow tables in the switch, but no match is found. Describe the most common options for handling this packet. (Note: review the OpenFlow Switch Specification and the textbook for information on packet processing in OpenFlow switches.)



---

#### EXTRA CREDIT:
#### 7.) In lecture, we will demonstrate a SIP softphone calling other SIP clients. Create an account for yourself on a SIP service provider (such as www.iptel.org) and using a SIP phone of your choice, call us at sip:cs40@iptel.org and leave us a voicemail message.

I was unable to make a successful call to cs40@iptel.org, but was able to connect to music@iptel.org
<img width="785" alt="screen shot 2018-08-01 at 9 39 48 pm" src="https://user-images.githubusercontent.com/5629547/43557646-a124d99e-95d3-11e8-8b36-2820a9396d51.png">
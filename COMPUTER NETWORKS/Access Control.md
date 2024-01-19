---
sr-due: 2024-01-11
sr-interval: 1
sr-ease: 230
---

- #review #flashcards
- used for multipoint link
- **CSMA/CA**
?
	- Carrier Sense Multiple Access with Collision  Avoidance
	-
	- ==*Carrier Sense*== = Before a network device tries to send data over the Ethernet, it first checks to see if another device is already transmitting on the network (i.e., it "senses the carrier"). If the network is free, the device starts transmitting its data.
	- ==*Multiple Access* === multiple devices are accessing the network. In a CSMA/CD environment, multiple devices can be connected to and communicate over the same network.
	- ==*Collision Avoidance (CA)==:* Since detecting [[collisions]] in a wireless environment is more challenging than in a wired environment, CSMA/CA takes a different approach. Instead of detecting collisions and then dealing with them, it tries to prevent them from happening in the first place.
<!--SR:!2024-01-12,2,230-->

  -          **Interframe Space (IFS)**: A small waiting time is introduced before a device starts transmitting data. This gap reduces the chance of two devices transmitting at the same time.
    
-           **Random Backoff**: If the medium is busy, the device waits for a random period before trying to transmit again. This randomness reduces the likelihood of two devices choosing the same time to start transmission, thus minimizing collisions.
    
-         **Request to Send/Clear to Send (RTS/CTS)**: In networks with heavy traffic, an optional RTS/CTS mechanism can be used. A device first sends a short RTS frame to the access point, indicating its intent to transmit. The access point then replies with a CTS frame, giving permission to the requesting device while alerting other devices to hold off from transmitting for a specified duration.
-**CSMA/CD**
	- CSMA same as before
	- CD : Since multiple devices can transmit data at any time, there's a chance that two or more devices might try to send data simultaneously, leading to a collision. When a device detects that a collision has occurred, it stops transmitting and waits for a random period before trying to send the data again.
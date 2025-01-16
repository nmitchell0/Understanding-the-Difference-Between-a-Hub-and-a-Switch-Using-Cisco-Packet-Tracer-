# Understanding-the-Difference-Between-a-Hub-and-a-Switch-Using-Cisco-Packet-Tracer-
In this project, I explored the differences between a hub and a switch using Cisco Packet Tracer. I used practical examples and command-line tools, like ping, to test how data is sent and received on a network.

Overview

In this project, I explored the differences between a hub and a switch using Cisco Packet Tracer. I used practical examples and command-line tools, like ping, to test how data is sent and received on a network.

Key Learnings

	1.	Hub Behavior:
	•	A hub broadcasts all messages to all devices in the network, even if only one device is the intended recipient.
	•	For example, I used ping 10.1.2.5 from Laptop 1 to Laptop 3, but the message was also sent to two other devices on the network.
	2.	Switch Behavior:
	•	A switch uses MAC addresses to send the message directly to the intended device.
	•	For example, I used ping 10.1.1.5 from Computer 1 to Computer 3, and the message went directly to Computer 3 without involving other devices.
	3.	Layer 2 and Layer 3 Concepts:
	•	The switch uses Layer 2 (MAC address) to deliver the message to the destination.
	•	Once the message reaches the recipient, Layer 3 (IP address) is used to ensure the message is intended for them and to understand its content.
	•	When the recipient replies, the same process is followed in reverse.

Practical Skills

	•	Used ping to test connectivity between devices.
	•	Observed how a hub broadcasts messages versus how a switch directs messages.
	•	Gained hands-on experience with Cisco Packet Tracer for networking simulations.

Conclusion

This project helped me understand the practical differences between a hub and a switch and how each operates within a network. Using Layer 2 (MAC addresses) and Layer 3 (IP addresses) was critical to grasping how data is sent and received efficiently.

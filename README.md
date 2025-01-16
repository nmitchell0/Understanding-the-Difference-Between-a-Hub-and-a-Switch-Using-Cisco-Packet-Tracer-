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


Commands Used in Cisco Packet Tracer

1. Pinging a Device

The ping command is used to test connectivity between devices on a network. Here’s an example:

ping 10.1.2.5
This sends a message to the device with the IP address 10.1.2.5 to check if it is reachable.

2. Checking ARP Table (Switch)

You can view the ARP (Address Resolution Protocol) table to see which MAC addresses are linked to which IP addresses:

arp -a
This command helps confirm how the switch maps Layer 2 (MAC) and Layer 3 (IP) addresses.

3. Observing Broadcast Behavior (Hub)

When using a hub, the ping command sends the message to all devices on the network, even if it’s intended for one device. Example:

ping 10.1.2.5

Output (hub behavior):

Reply from 10.1.2.5: bytes=32 time<1ms TTL=128
Reply from 10.1.2.4: Destination host unreachable
Reply from 10.1.2.3: Destination host unreachable

This shows the message was sent to all devices, but only 10.1.2.5 responded.

4. Testing Direct Communication (Switch)

When using a switch, the ping command sends the message directly to the intended device based on its MAC address.

{ping 10.1.1.5}

Output (switch behavior):

Reply from 10.1.1.5: bytes=32 time<1ms TTL=128
Here, the message is sent only to the device with IP 10.1.1.5.

5. Viewing the MAC Address Table on the Switch

On a switch, you can use this command to see the MAC address table:

show mac address-table

This displays which MAC addresses are connected to which ports on the switch, confirming how the switch routes traffic.
Example output:

VLAN    MAC Address       Type        Ports
1       00A0.C9A1.1234    Dynamic     FastEthernet0/1
1       00A0.C9B2.5678    Dynamic     FastEthernet0/2

Suggested Workflow for Testing

1.	Set up the devices in Cisco Packet Tracer:
	•	Connect devices using a hub or switch.
	•	Assign unique IP addresses to each device.
3.	Test with a Hub:
   
	•	Use the ping command to send a message to a specific IP address.
	•	Observe how the hub broadcasts the message to all devices.
4.	Test with a Switch:
   
	•	Replace the hub with a switch and repeat the test using ping.
	•	Observe how the switch directs the message only to the intended recipient.
5.	Check Address Tables:
   
	•	Use show mac address-table on the switch to see how it tracks devices.
	•	Use arp -a on a device to verify how IP and MAC addresses are resolved.

Small Business Network Infrastructure Design

A Cisco Packet Tracer project that demonstrates the design, configuration, and testing of a small business LAN using a router, switch, and end-user devices.

📌 Project Overview

This project simulates a basic small-business network where multiple users connect through a network switch and router.

Main Objectives

Design a simple and reliable LAN topology

Connect end-user computers through a switch

Connect the LAN to a router

Configure IP addressing

Configure basic routing and switching

Verify end-to-end connectivity

Troubleshoot common connectivity problems

🖥️ Network Topology

The topology contains:

1 Router — Cisco ISR4321

1 Switch — Cisco 2960-24TT

2 PCs — User-A and User-B

Ethernet connections between the devices

Topology Diagram



🔧 Technologies & Tools

Technology / Tool

Purpose

Cisco Packet Tracer

Network design and simulation

TCP/IP

Network communication

LAN

Local network connectivity

IP Addressing

Device identification and communication

Ethernet

Wired device connectivity

Routing

Communication between networks

Switching

Communication inside the LAN

🏗️ Network Structure

             ┌───────────────┐
             │  Cisco Router │
             │   ISR4321     │
             └───────┬───────┘
                     │
                     │
             ┌───────┴───────┐
             │     Switch    │
             │   2960-24TT   │
             └───────┬───────┘
                  ┌──┴──┐
                  │     │
                User-A User-B
                  PC     PC

🚀 Project Setup — Step by Step

Step 1 — Open Cisco Packet Tracer

Install and open Cisco Packet Tracer.

Create a new Packet Tracer workspace.

Step 2 — Add Network Devices

From the Packet Tracer device menu, add:

One Cisco ISR4321 Router

One Cisco 2960-24TT Switch

Two PC-PT devices

Rename the PCs:

User-A

User-B

Rename the router:

Central-RT

Rename the switch:

Central-SW

Step 3 — Create the Physical Connections

Connect the devices using Ethernet cables.

Typical structure:

User-A ─────┐
            │
            ▼
         Central-SW ───── Central-RT
            ▲
            │
User-B ─────┘

Use the appropriate Ethernet interfaces available on each device.

Step 4 — Configure IP Addresses

Assign an IP address, subnet mask, and default gateway to each end device.

Example addressing scheme:

Device

IP Address

Subnet Mask

Default Gateway

User-A

192.168.1.10

255.255.255.0

192.168.1.1

User-B

192.168.1.11

255.255.255.0

192.168.1.1

Router LAN

192.168.1.1

255.255.255.0

—

Note: Use the exact addressing required by your Packet Tracer activity if it differs from this example.

Configure a PC

Go to:

PC → Desktop → IP Configuration

Enter:

IP Address

Subnet Mask

Default Gateway

Repeat the process for the second PC.

Step 5 — Configure the Router

Open:

Central-RT → CLI

Configure the required LAN interface with the network IP address.

Example:

enable
configure terminal
interface gigabitEthernet 0/0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit
end

Interface names can vary depending on the router model and Packet Tracer activity.

Step 6 — Configure the Switch

Open:

Central-SW → CLI

For basic LAN connectivity, connect the PCs and router to the appropriate switch ports.

If management access is required, configure a management IP on the switch.

Example:

enable
configure terminal
hostname Central-SW
exit

Additional switch configuration should follow the requirements of the specific network activity.

Step 7 — Verify Device Status

Check that:

Router interface is up

Switch ports are up

PC Ethernet links are active

Correct IP addresses are configured

Default gateways are correct

In Packet Tracer, green link indicators normally show an active connection.

🧪 Step 8 — Test Connectivity

Use the PC command prompt.

Go to:

PC → Desktop → Command Prompt

Test the Default Gateway

ping 192.168.1.1

A successful reply confirms communication between the PC and router.

Test PC-to-PC Communication

From User-A:

ping 192.168.1.11

A successful response confirms LAN connectivity between the users.

🔍 Step 9 — Troubleshooting

If the ping fails, check the following:

1. Check IP Address

Make sure the PC has the correct:

IP address

Subnet mask

Default gateway

2. Check Router Interface

Make sure the router interface is enabled:

show ip interface brief

Look for the interface status:

up    up

3. Check Cable Connections

Verify that the correct Ethernet cables and interfaces are being used.

4. Check Switch Ports

Verify that the connected switch ports are active.

5. Check the Gateway

The PC's default gateway must match the router interface address for its network.

📸 Project Screenshots

Network Topology



Connectivity / Configuration View



📥 Download Project

You can download and open the original Cisco Packet Tracer project file:

👉 Download Cisco Packet Tracer Project (.pkt)

Open the .pkt file with Cisco Packet Tracer.

📂 Repository Structure

small-business-network/
│
├── README.md
├── small-business-network_kk.pkt
│
├── Screenshot 2026-09-02 231908.png
└── Screenshot 2026-09-02 231924.png

🎯 Skills Demonstrated

Network topology design

Cisco Packet Tracer

IP addressing

TCP/IP fundamentals

LAN configuration

Router configuration

Switch configuration

Ethernet connectivity

Ping and connectivity testing

Basic network troubleshooting

📚 Learning Outcomes

After completing this project, the following networking concepts are demonstrated:

Understanding of LAN architecture

Understanding of routers and switches

Basic IP addressing

Default gateway configuration

Router interface configuration

Basic switch connectivity

End-to-end communication testing

Network troubleshooting

👨‍💻 Project Information

Project: Small Business Network Infrastructure Design
Platform: Cisco Packet Tracer
Network Type: LAN
Devices: Router, Switch, PCs
Status: Completed

⭐ Project Summary

Design → Configure → Connect → Test → Troubleshoot

This project demonstrates how a small business can build a basic wired network infrastructure using Cisco networking devices and end-user systems.

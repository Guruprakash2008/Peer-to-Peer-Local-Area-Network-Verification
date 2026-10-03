# Peer-to-Peer Local Area Network Verification

## 📌 Project Overview

This project demonstrates the configuration and verification of a simple **Peer-to-Peer Local Area Network (LAN)** using Cisco Packet Tracer.

Two workstations, **PC0 and PC1**, are connected through a **Cisco 2960 Layer 2 switch**. Both PCs are configured with static IPv4 addresses in the same subnet, and connectivity is verified using the `ping` command.


## 🎯 Objective

The objectives of this project are:

* To create a basic Local Area Network using Cisco Packet Tracer.
* To connect two PCs through a Layer 2 switch.
* To configure static IPv4 addresses.
* To configure subnet masks and default gateways.
* To verify network connectivity using the `ping` command.
* To troubleshoot basic connectivity problems.


## 🛠️ Software Used

* **Cisco Packet Tracer**
* IPv4 Networking

## 🌐 Network Topology

        PC0
   192.168.10.25
          |
          | Fa0/1
          |
     +----------+
     | Switch0  |
     | 2960     |
     +----------+
          |
          | Fa0/2
          |
        PC1
   192.168.10.26


## 📦 Devices Used

| Device                        | Quantity |
| ----------------------------- | -------: |
| PC                            |        2 |
| Cisco 2960 Switch             |        1 |
| Copper Straight-Through Cable |        2 |


## 💻 IP Address Configuration

| Device  | Interface     | IPv4 Address  | Subnet Mask   | Default Gateway |
| ------- | ------------- | ------------- | ------------- | --------------- |
| PC0     | FastEthernet0 | 192.168.10.25 | 255.255.255.0 | 192.168.10.1    |
| PC1     | FastEthernet0 | 192.168.10.26 | 255.255.255.0 | 192.168.10.1    |
| Switch0 | —             | Default       | —             | —               |

Both PCs belong to the same network:

192.168.10.0/24



## 🔌 Physical Connections

The devices are connected using **Copper Straight-Through** cables.


PC0 FastEthernet0 → Switch0 FastEthernet0/1



The switch ports should become **green** after the network converges.

---

# ⚙️ Implementation Procedure

## Step 1: Place the Devices

Open Cisco Packet Tracer.

Add:

* PC0
* PC1
* Cisco 2960 Switch

Place the switch between the two PCs.

---

## Step 2: Connect the Devices

Select:

**Connections → Copper Straight-Through**

Connect:

```text
PC0 Fa0 → Switch0 Fa0/1
PC1 Fa0 → Switch0 Fa0/2
```

Wait for the link indicators to become green.

---

## Step 3: Configure PC0

Open:

**PC0 → Desktop → IP Configuration**

Select **Static** and enter:

```text
IP Address:       192.168.10.25
Subnet Mask:      255.255.255.0
Default Gateway:  192.168.10.1
```

---

## Step 4: Configure PC1

Open:

**PC1 → Desktop → IP Configuration**

Select **Static** and enter:

```text
IP Address:       192.168.10.26
Subnet Mask:      255.255.255.0
Default Gateway:  192.168.10.1
```

---

# 🧪 Verification

## Step 5: Check PC0 Configuration

Open:

**PC0 → Desktop → Command Prompt**

Run:

```text
ipconfig
```

Verify that PC0 has:

```text
IP Address: 192.168.10.25
Subnet Mask: 255.255.255.0
```

---

## Step 6: Test PC0

Test PC0's own IP address:

```text
ping 192.168.10.25
```

Expected result:

```text
Reply from 192.168.10.25
```

This confirms that PC0's IP configuration is working.

---

## Step 7: Test PC1 from PC0

From the PC0 Command Prompt, run:

```text
ping 192.168.10.26
```

Expected output:

```text
Reply from 192.168.10.26: bytes=32 time<1ms TTL=128
Reply from 192.168.10.26: bytes=32 time<1ms TTL=128
Reply from 192.168.10.26: bytes=32 time<1ms TTL=128
Reply from 192.168.10.26: bytes=32 time<1ms TTL=128
```

A successful response confirms connectivity between PC0 and PC1.

---

# 🔍 Troubleshooting

If the ping fails, check the following:

### 1. Check the Cable

Make sure Copper Straight-Through cables are used.

### 2. Check Link Lights

The connections should become green.

### 3. Check IP Addresses

PC0:

```text
192.168.10.25
```

PC1:

```text
192.168.10.26
```

### 4. Check Subnet Masks

Both PCs should have:

```text
255.255.255.0
```

### 5. Check Network

Both PCs must belong to:

```text
192.168.10.0/24
```

### 6. Test Again

Run:

```text
ping 192.168.10.26
```

from PC0.

---

# 📸 Screenshots

The following screenshots can be included in the project:

<img width="1366" height="729" alt="image" src="https://github.com/user-attachments/assets/dda08def-9d4e-4276-a9c3-1c4e608cde18" />


Recommended folder structure:

```text
screenshots/
│
├── 01_Topology.png
├── 02_PC0_IP_Configuration.png
├── 03_PC1_IP_Configuration.png
├── 04_PC0_ipconfig.png
└── 05_Successful_Ping.png
```

---

# 📂 Project Files

```text
Peer-to-Peer-LAN/
│
├── README.md
├── Peer_to_Peer_LAN.pkt
│
└── screenshots/
    ├── 01_Topology.png
    ├── 02_PC0_IP_Configuration.png
    ├── 03_PC1_IP_Configuration.png
    ├── 04_PC0_ipconfig.png
    └── 05_Successful_Ping.png
```

---

# 📚 Concepts Covered

* Local Area Network (LAN)
* IPv4 Addressing
* Static IP Configuration
* Subnet Mask
* Layer 2 Switch
* FastEthernet
* Copper Straight-Through Cable
* `ipconfig` command
* `ping` command
* Basic Network Troubleshooting

---

# ✅ Result

A peer-to-peer Local Area Network was successfully created using two PCs and a Cisco 2960 Layer 2 switch. Static IPv4 addresses were configured on both workstations, and connectivity was successfully verified using the `ping` command.

---

## 👨‍💻 Author

**Guruprakash**

**Course:** B.Tech – Computer Science and Business Systems

---

## 📌 Project Status

**Completed ✅**

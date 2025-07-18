# 🧪 Exploring DNS Traffic with Wireshark

## 📖 Overview
This lab focused on analyzing **DNS (Domain Name System)** traffic using **Wireshark**, a network protocol analyzer. The goal was to understand how DNS queries and responses are exchanged, how to identify them in packet captures, and how DNS supports everyday internet activities.

## 🔧 Tools Used
- **Wireshark**
- **Cisco Networking Academy Lab Environment**
- **Web Browser / Command Line (nslookup / dig)**

## 🧬 Lab Steps

### 1. Start Packet Capture
- Launched Wireshark and selected the correct network interface.
- Applied the filter `dns` to view only DNS-related packets.

### 2. Generate DNS Traffic
- Opened websites and used `nslookup` or `dig` commands to initiate DNS queries.
- Triggered both A (IPv4) and AAAA (IPv6) queries.

### 3. Analyze DNS Packets
- Inspected DNS queries and responses:
  - **Query Type**: A, AAAA, CNAME, NS
  - **Transport Protocol**: Mostly UDP/53 (some TCP/53 for larger payloads)
  - **Flags**: Standard query, response, recursion desired
  - **Answers**: IP addresses, CNAME chains, TTLs

### 4. Follow DNS Streams
- Used **"Follow UDP Stream"** to trace full DNS conversations.
- Observed recursive queries and redirections via CNAME.

### 5. Identify Patterns and Issues
- Observed:
  - Multiple answers in one response
  - DNS cache behavior using TTL
  - Failed queries and timeouts

## 📚 Key Takeaways
- DNS is essential for translating domain names to IP addresses.
- Wireshark provides deep insights into DNS traffic structure and flow.
- TTL helps optimize DNS caching to reduce lookup delays.
- CNAME records can redirect queries, which adds steps in resolution.


## ✅ Status: Completed
This was part of the **Cisco Networking Academy cybersecurity labs**, and helped me gain hands-on experience in network traffic analysis.


# 🌐 Network Basics Guide

This guide covers essential networking concepts and hands-on tools for debugging and securing systems.  

---

## 📘 Theory

### 🔹 OSI vs. TCP/IP Models
- **OSI (7 Layers):** Physical → Data Link → Network → Transport → Session → Presentation → Application  
- **TCP/IP (4 Layers):** Network Interface → Internet → Transport → Application  
- Mapping: OSI Network ↔ TCP/IP Internet, OSI Transport ↔ TCP/IP Transport  

---

### 🔹 IP Addresses & Subnetting (Brief)
- **IPv4:** 32-bit (e.g., `192.168.1.1`)  
- **IPv6:** 128-bit (e.g., `2001:db8::1`)  
- **Subnetting:** Divides networks into smaller subnets  
  - Example: `192.168.1.0/24` → 256 IPs (254 usable)  
- **CIDR Notation:** `/24 = 255.255.255.0`  

---

### 🔹 Ports and Protocols
- **TCP:** Reliable, connection-oriented (e.g., HTTP, HTTPS, SSH).  
- **UDP:** Fast, connectionless (e.g., DNS, DHCP, streaming).  
- **Common Ports:**  
  - 22 → SSH  
  - 53 → DNS  
  - 80 → HTTP  
  - 443 → HTTPS  

---

### 🔹 DNS Concept
- **Domain Name System (DNS):** Resolves domain names → IP addresses  
- Lookup order: Local cache → Resolver → Root → TLD → Authoritative server  

---

## 🛠️ Tools

### 🔹 Connectivity Testing
- `ping <host>` → Test ICMP reachability, latency, packet loss  
- `traceroute <host>` → Trace path of packets (hops)  
- `mtr <host>` → Continuous traceroute with stats  

---

### 🔹 Application Tools
- `curl -I https://example.com` → Fetch HTTP headers  
- `wget https://example.com/file.zip` → Download files  
- `dig example.com A` → Query DNS records  
- `nslookup example.com` → Simple DNS lookup  
- `telnet example.com 80` → Test raw port connectivity  
- `nc -zv example.com 443` → Check if port is open  

---

### 🔹 Socket / Listening Tools
- `ss -tulpn` → Show listening sockets (modern replacement for netstat)  
- `netstat -tulnp` → Show active connections and listening ports  
- `lsof -i :80` → Check which process is using port 80  

---

### 🔹 Firewall Basics (UFW)
- Enable firewall:  
  ```bash
  sudo ufw enable
- Allow ssh:
`sudo ufw allow 22/tcp`
- Deny all other incoming traffic:
  `sudo ufw default deny incoming`
- Show status:
  `sudo ufw status`

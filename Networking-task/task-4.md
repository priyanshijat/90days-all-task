# 🧠 Networking Commands Cheat Sheet

A quick reference guide to essential networking commands for Linux.

---

## 🔄 ping – Check Network Connectivity

**Purpose**: Tests if a host is reachable and measures latency.

```bash
ping <hostname or IP>
# Example:
ping google.com

```

## traceroute / tracert – Trace Packet Routes

**Purpose**: Displays the route and transit delays of packets.

```bash
# Linux/macOS:
traceroute <hostname or IP>

# Windows:
tracert <hostname or IP>

# Example:
traceroute google.com
```

## netstat – Network Statistics
**Purpose**: Shows active connections, ports, and interface statistics.
```bash
netstat -an       # Show all connections and listening ports
netstat -rn       # Display routing table
netstat -tulnp    # Linux: Show listening ports with process info
```

## 🌐 curl – Make HTTP Requests
**Purpose**: Transfers data to or from a server.
```bash
curl <URL>
```

## 🧭 dig – DNS Lookup (Linux/macOS)
**Purpose**: Queries DNS for info about hostnames.
```bash
dig <domain>
```

## 🕵️ nslookup – DNS Lookup (Cross-platform)
**Purpose**: Gets domain name or IP address mapping.
```bash
nslookup <domain>
```

## 🔎 ifconfig / ip a – View Network Interfaces
**Purpose**: Displays or configures network interfaces.
```bash
ifconfig       # (older)
ip a           # modern replacement
```

## 🧮 ip / ipconfig – Show IP Configuration
**Purpose**: Shows IP, gateway, and interface info.
```bash
# Windows:
ipconfig /all

# Linux:
ip addr
ip route
```
## 🏹 telnet – Check Port Connectivity
**Purpose**: Tests connection to a specific port on a host.
```bash
telnet <hostname> <port>
# Example:
telnet google.com 80
```

## 🔐 ssh – Secure Shell
**Purpose**: Connects securely to remote machines.
```bash
ssh <user>@<hostname>
```

## 📤 scp – Secure File Copy
**Purpose**: Transfers files between computers over SSh.
```bash
scp file.txt user@host:/path/
```

## 🚦 nmap – Network Scanner
**Purpose**: Scans open ports and services on a network.
```bash
nmap <target>
nmap -sS -p- <IP>     # Full TCP port scan
```

## 📥 wget – File Downloader
**Purpose**: Downloads files from the web via HTTP/HTTPS/FTP.
```bash
wget <URL>

```

All the basic commands of Netwoking......
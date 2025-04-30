# 🌐 Linux Networking Commands

This section includes essential commands for checking IPs, managing interfaces, testing connectivity, and diagnosing network issues.

---

```bash

🌍 Check Network Configuration

ip a                       # Show all IP addresses (modern alternative to ifconfig)
ifconfig                   # Show network interfaces (legacy, may require net-tools)
hostname -I                # Show IP address
ip route                   # Display routing table

🌐 DNS & Name Resolution

nslookup google.com        # DNS lookup (hostname to IP)
dig google.com             # Detailed DNS query
host google.com            # Simple DNS lookup

📶 Ping & Connectivity Testing

ping google.com            # Send ICMP packets
ping -c 5 8.8.8.8          # Ping with a count
traceroute google.com      # Trace route to host
mtr google.com             # Real-time traceroute (needs install)

🌐 Port & Service Checks

telnet google.com 80       # Check TCP port (if telnet is installed)
nc -zv google.com 443      # Netcat: check if port is open
ss -tuln                   # Show listening ports
netstat -tulnp             # Show active connections (legacy)

🔄 Download & Transfer

curl ifconfig.me           # Get external IP via curl
curl -O http://example.com/file.txt   # Download file with original name
wget http://example.com/file.txt      # Download using wget
scp file.txt user@host:/path/         # Copy file over SSH
rsync -avz file/ user@host:/path/     # Sync files over SSH

🔧 Interface Management (requires sudo)

ip link set eth0 down      # Disable interface
ip link set eth0 up        # Enable interface
dhclient eth0              # Request IP via DHCP

🧪 Troubleshooting Tools

arp -a                     # Show ARP cache
ip neigh                  # Neighbor table (MAC resolution)
ethtool eth0              # Check interface driver/settings

💡 Use sudo when needed, especially for interface or service changes.

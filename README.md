Here's a README for your **Packet Sniffer** program:

---

# Network Packet Sniffer

## Description

This is a simple Python-based **Network Packet Sniffer** that captures and analyzes network packets. It uses the **Scapy** library to capture packets, and it displays information such as source and destination IP addresses, protocols (ICMP, TCP, UDP), packet sizes, and any raw payload data. This tool is useful for educational purposes and allows users to understand how network traffic flows in a network.

**Note:** This program should only be used on networks where you have permission to capture traffic, as unauthorized packet sniffing may violate privacy laws or network policies.

## Features

- Capture network packets over the network.
- Display relevant packet information including:
  - Source IP
  - Destination IP
  - Protocol (ICMP, TCP, UDP)
  - Packet Size
  - Payload Data (if available)
- Support for IPv4 (captures packets of type `IP`).
- Displays timestamp for each captured packet.
- Filters out non-IP packets.

## Requirements

- Python 3.x
- Scapy library

You can install Scapy using pip:

```bash
pip install scapy
```

### Running the Script

To run the packet sniffer, you'll need **root** or **administrator** privileges, as packet capturing requires access to raw sockets.

### Linux/MacOS:
Run the script using `sudo` to allow it to capture packets:

```bash
sudo python3 packet_sniffer.py
```

### Windows:
Make sure you're running the script in an **Administrator Command Prompt** to allow access to raw sockets.

### Program Flow

1. **Start Sniffing**: The program begins capturing packets once executed.
2. **Packet Analysis**: Each captured packet is analyzed and relevant information such as source and destination IPs, protocol type, and packet size is displayed.
3. **Payload**: If the packet contains raw data (payload), it is also displayed.

### Example Output

```text
Starting packet sniffer... Press Ctrl+C to stop.
Time: 2024-11-07 12:30:15
Source IP: 192.168.0.1, Destination IP: 192.168.0.2
Protocol: TCP, Packet Size: 80 bytes
No Payload Data

Time: 2024-11-07 12:30:16
Source IP: 192.168.0.2, Destination IP: 192.168.0.1
Protocol: UDP, Packet Size: 150 bytes
Payload Data: b'\x00\x01\x02...'
```

### Troubleshooting

- **Permission Denied**: If you encounter `Permission denied` or similar errors, ensure that you're running the script with the appropriate privileges (i.e., as root or administrator).
  
- **Non-IP Packets**: The script filters for IP packets only. Other types of packets (e.g., ARP or Ethernet frames) will be ignored.

## Disclaimer

This tool is designed for **educational purposes** only. You should only run this tool on networks that you own or have explicit permission to capture traffic from. Unauthorized packet sniffing may violate laws or network policies and can lead to legal consequences.

## License

This project is open-source and available under the MIT License.

---

You can copy and paste this README into a `README.md` file in your project directory. This should provide clear instructions on using and understanding the Packet Sniffer program.

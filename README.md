Network Packet Analyzer 🔍
==========================

Project Overview
----------------

The **Network Packet Analyzer** is a Python-based tool that captures and analyzes network packets in real-time, displaying key information such as source and destination IP addresses, MAC addresses, protocols, and payload data. This project aims to provide insights into network traffic and deepen understanding of network analysis techniques in a controlled and ethical environment.

Features
--------

-   **Real-time Packet Capture**: Captures live network traffic from specified interfaces.
-   **Protocol Analysis**: Supports TCP, UDP, and ICMP protocols.
-   **Detailed Packet Information**: Displays source and destination IP and MAC addresses, protocols, and payload data.
-   **Customizable Interface**: Easily configurable for different network interfaces, allowing you to capture data from wired and wireless networks.

Installation
------------

Ensure you have Python 3.x and Scapy installed on your machine. Scapy requires root privileges for network sniffing, so installation may require `sudo`.

### 1\. Clone the Repository

bash

Copy code

`git clone https://github.com/yourusername/network-packet-analyzer.git
cd network-packet-analyzer`

### 2\. Install Dependencies

bash

Copy code

`pip install scapy`

Usage
-----

1.  **Run the script with root privileges** to allow packet sniffing.

    bash

    Copy code

    `sudo python3 packet-sniffer.py`

2.  **Specify the network interface** (default is `eth0`). Modify the `interface` variable if you need to switch to another interface (e.g., `wlan0` for Wi-Fi).

3.  **Output Example**: The tool will display captured packet information in the console.

    plaintext

    Copy code

    `[*] Starting packet capture on eth0...

    [+] Packet captured at: 2024-10-21 12:47:44
    Source MAC: 00:0c:29:af:fe:07
    Destination MAC: ff:ff:ff:ff:ff:ff
    Protocol: TCP
    Payload: b'GET / HTTP/1.1...'
    ------------------------------------------------------------`

File Structure
--------------

-   `packet-sniffer.py`: Main Python script for capturing and analyzing network packets.

Ethical Considerations ⚠️
-------------------------

This tool is built for educational purposes in controlled environments. Unauthorized packet sniffing is illegal and a violation of privacy laws. Ensure you have permission to capture packets on the network you're analyzing.

License
-------

This project is licensed under the MIT License. See LICENSE for more details.

Contributing
------------

Contributions are welcome! Feel free to submit a pull request or open an issue to suggest improvements or report bugs.

* * * * *

### Example Snippet

python

Copy code

`# Packet Sniffer Tool
from scapy.all import sniff

def analyze_packet(packet):
    # Analyzes each captured packet and displays relevant information
    print(packet.summary())

# Start packet capture on specified interface
sniff(iface='eth0', prn=analyze_packet, count=10)`

* * * * *

### Connect with Me

Feel free to reach out if you'd like to collaborate or discuss network security topics!

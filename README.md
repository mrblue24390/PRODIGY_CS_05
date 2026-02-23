# 🌐 Network Packet Analyzer

<div align="center">

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Tests](https://img.shields.io/github/actions/workflow/status/yourusername/Network-Packet-Analyzer/python-ci.yml)
![Scapy](https://img.shields.io/badge/scapy-2.5.0+-orange)

**An educational tool for capturing and analyzing network packets with Python and Scapy**

[Features](#features) • [Installation](#installation) • [Quick Start](#quick-start) • [Documentation](#documentation) • [Ethical Use](#ethical-use)

</div>

---

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Quick Start](#quick-start)
- [How It Works](#how-it-works)
- [Usage Examples](#usage-examples)
- [Project Structure](#project-structure)
- [Ethical Guidelines](#ethical-guidelines)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

---

## 🎯 Overview

The **Network Packet Analyzer** is a Python-based tool that captures and analyzes network packets in real-time. It provides detailed information about network traffic including source/destination IP addresses, protocols, ports, and payload data. This tool is designed for **educational purposes** to help understand network protocols and traffic analysis.

### ⚠️ IMPORTANT ETHICAL NOTICE
This tool is intended **ONLY** for:
- ✅ Learning about network protocols
- ✅ Analyzing your own network traffic
- ✅ Educational environments with proper authorization
- ✅ Security research on networks you own or have explicit permission to test

**UNAUTHORIZED use of packet sniffers may be ILLEGAL and UNETHICAL.**

---

## ✨ Features

### 🔍 Packet Capture
| Feature | Description |
|---------|-------------|
| **Real-time sniffing** | Capture live network traffic |
| **Multiple interfaces** | Select specific network interfaces |
| **Packet filtering** | Filter by protocol, IP, port, etc. |
| **Count limits** | Stop after specified number of packets |

### 📊 Packet Analysis
- **Ethernet Layer**: Source/destination MAC addresses
- **IP Layer**: Source/destination IP addresses, TTL, protocol
- **TCP/UDP**: Port numbers, flags, sequence numbers
- **ICMP**: Type, code, payload
- **Payload data**: Hex and ASCII representation

### 🛠️ Output Options
- Console display with formatted output
- Save to PCAP file for later analysis
- Export to JSON/CSV for data processing
- Protocol-specific summaries

---

## 🛠️ Technology Stack

| Technology | Version | Purpose |
|------------|---------|---------|
| **Python** | 3.8+ | Core programming language |
| **Scapy** | 2.5.0+ | Packet manipulation and sniffing |
| **pytest** | 7.0+ | Unit testing framework |
| **GitHub Actions** | - | CI/CD automation |

---

## 📦 Installation

### Prerequisites
- Python 3.8 or higher
- Administrator/root privileges (required for packet capture on most systems)
- Npcap (Windows) or libpcap (Linux/macOS)

### Step 1: Install Dependencies

#### On Linux:
```bash
sudo apt-get update
sudo apt-get install python3-pip libpcap-dev

# Clone the repository
git clone https://github.com/mrblue24390/PRODIGY_CS_05.git
cd PRODIGY_CS_05

# (Optional) Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install Python dependencies
pip install -r requirements.txt

#### Verify Installation
# Run with appropriate privileges
# On Linux/macOS:
sudo python code.py --info

# On Windows (run as Administrator):
python code.py --info

####Capture 10 Packets
sudo python code.py --count 10
###Capture with Filter (HTTP traffic only)
sudo python code.py --filter "tcp port 80" --count 5




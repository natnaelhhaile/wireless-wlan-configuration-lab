# Wireless Router & WLAN Configuration Lab

## Overview

This project demonstrates the configuration and validation of a basic wireless LAN (WLAN) environment using a wireless router and two client devices (wired PC and wireless laptop). The lab focuses on configuring SSID settings, wireless security (WPA2), DHCP services, and verifying end-to-end connectivity across wired and wireless clients.

The objective is to simulate a small enterprise or home-office wireless network and validate core networking concepts including IP addressing, DHCP allocation, and wireless client authentication.

---

## Topology

The network consists of:

- One wireless router acting as DHCP server and access point
- One wired desktop computer connected via Ethernet
- One wireless laptop connected via Wi-Fi

📌 Topology Diagram:
(Insert topology screenshot here)

---

## Addressing Scheme

- Router IP Address: `192.168.50.1`
- Subnet Mask: `255.255.255.0`
- DHCP Pool: `192.168.50.100 – 192.168.50.149`
- SSID: `NET352`
- Security: WPA2-PSK (AES)
- Passphrase: `Cisco456!`

---

## Implementation Steps

### 1. Router Access and Initial Configuration

The wireless router was accessed via its default gateway using a wired connection from the desktop client. The default credentials were used for initial login and verification of connectivity.

📌 Evidence:
- Default gateway validation via `ipconfig`
- Router login interface access

---

### 2. SSID Configuration

The wireless network name (SSID) was configured as:

- SSID: `NET352`

This allows wireless clients to identify and connect to the correct access point.

📌 Screenshot:
(Insert SSID configuration screenshot here)

---

### 3. Wireless Security Configuration

Wireless security was configured using WPA2-Personal with AES encryption to ensure secure authentication and encrypted communication between wireless clients and the router.

- Security Mode: WPA2-PSK
- Encryption: AES
- Passphrase: `Cisco456!`

📌 Screenshot:
(Insert WPA2 configuration screenshot here)

---

### 4. DHCP Configuration

The router was configured to act as a DHCP server, dynamically assigning IP addresses to connected clients within the defined subnet.

- Router IP: `192.168.50.1`
- DHCP range: `192.168.50.100 – 192.168.50.149`

After applying configuration changes, clients renewed their IP addresses successfully using `ipconfig /renew`.

📌 Screenshot:
(Insert DHCP configuration screenshot here)

---

### 5. Wireless Client Connection

The wireless laptop successfully detected the configured SSID (`NET352`), authenticated using the WPA2 passphrase, and obtained an IP address via DHCP.

📌 Screenshot:
(Insert wireless network scan screenshot here)

---

### 6. IP Address Verification (Wireless Client)

After successful connection, the wireless client received the following network configuration:

- IP Address: `192.168.50.100`
- Subnet Mask: `255.255.255.0`
- Default Gateway: `192.168.50.1`

This confirms successful DHCP allocation and routing connectivity.

📌 Screenshot:
(Insert ipconfig output screenshot here)

---

## Troubleshooting Considerations

During WLAN deployment, common issues that may arise include:

- Incorrect SSID configuration or mismatch
- WPA2 authentication failure due to incorrect passphrase
- DHCP misconfiguration or disabled service
- IP address conflicts or lease exhaustion
- Wireless adapter disabled or driver issues on client device

---

## Key Networking Concepts Demonstrated

- Wireless LAN (WLAN) configuration
- SSID setup and management
- WPA2-PSK security implementation
- DHCP server configuration and IP allocation
- Client-side network troubleshooting
- Wired vs wireless connectivity validation

---

## Reflection

A laptop cannot connect to a wireless router. What troubleshooting steps should be taken?

- Verify that the wireless adapter is enabled and functioning on the client device
- Ensure the correct SSID is selected and visible
- Confirm correct WPA2 passphrase is used
- Check that DHCP is enabled on the router
- Validate router IP configuration and subnet settings
- Restart wireless interface or renew DHCP lease if necessary
- Inspect router wireless settings for MAC filtering or access restrictions

---

## Author

NATNAEL HAILE
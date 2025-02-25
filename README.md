Introduction

The IoT Firewall Gateway system integrates essential parts to create a solid, functional, and effective security solution. This system possesses numerous aspects and components that can be comprehensively analyzed and discussed over.

System Functionality

The system's main functionality is its ability to configure and manage firewall rules. Administrators have the ability to establish network zones, make modifications to rules, and set up automatic rule enforcement on a timetable. This feature guarantees strong network security by managing traffic and blocking unauthorized access. The system's firewall setup features are enhanced by regular security audits that verify the effectiveness of the firewall rules, ensuring that the network remains secure and follows the requirements of the industry.

Additionally, the system provides VPN settings for enabling secure remote access. Administrators can establish different VPN protocols, adjust server configurations, and monitor client access. This functionality ensures a secure connection to the network, protecting the data as it travels through encrypted routes. The VPN setup is closely connected with user authentication procedures, ensuring that only authorized users can access the network through the VPN.

Furthermore, the management of user authentication is an essential and crucial aspect of the system. This functionality enables administrators to establish and monitor user accounts, assign roles and permissions, and set authentication mechanisms. The system ensures that access to network resources is monitored and controlled by reorganizing user administration, therefore lowering the risk of unauthorized access and potential security breaches.

Data Recovery and Secure Internet Utilization

The system includes a comprehensive data recovery functionality. System configurations and data are regularly backed up in order to ensure the integrity and accessibility of the data. If there is a security breach or system failure, the recovery capability enables administrators to revert configurations and data to a previous state, reducing downtime and safeguarding important information.

Moreover, the system facilitates secure internet utilization for both administrators and end-users. The system provides a secure browsing experience by utilizing established firewall rules and VPN settings to monitor and regulate all network traffic. The system records user activities to facilitate audits, thereby enhancing accountability and transparency.

Security Mechanisms

The IoT Firewall Gateway solution incorporates multiple security mechanisms to ensure data integrity and protect against potential threats. Regular security audits, along with careful monitoring and logging, assist in rapidly discovering and fixing issues. The system's security has been improved by the addition of data recovery and strong authentication procedures, which ensure that it can effectively prevent and respond to security problems.

System Design
![image](https://github.com/user-attachments/assets/1bb23309-11f2-4de5-8fde-5c1b11d151c9)


Use-Case Diagram 
![image](https://github.com/user-attachments/assets/796316ed-83c6-40c7-83d0-f2c845ffd208)


Activity diagram 
![image](https://github.com/user-attachments/assets/50540a48-f6fc-4d5a-a541-b659635f0d38)

Interface Design (UI)

Starting this section, OpenWRT is provided with a pre-configured, web-based interface called LuCI. The researcher will use this web interface once they have installed the required LuCI packages, taking advantage of its capabilities to administer and configure the IoT firewall. LuCI provides a user-friendly interface to engage with the OpenWRT system, allowing access to a range of settings pages and critical functionality for this research. Following successfully installing LuCI, the researcher proceeded to explore many essential components of the interface, such as the Network Page, wireless Page, firewall Page, system management, VPN Page, audit Page, and management pages. These features enabled the effective setup and administration of the IoT firewall, ensuring a network environment that is both safe and dependable. This interface not only simplified the setup process but also offered multiple choices to manage network administration and security.

Login Page
![image](https://github.com/user-attachments/assets/36f7d1a9-7fc7-4a70-b35d-0500fd68142a)

Home Page
![image](https://github.com/user-attachments/assets/bb85d731-e796-439c-a2f3-34c32f87adfe)

Wireless page
![image](https://github.com/user-attachments/assets/2fd7eaaf-a064-4f76-992f-b0569ff4d0b0)

Firewall page
![image](https://github.com/user-attachments/assets/ac4081cd-cd5a-466c-a5ab-32e9a6a8a899)

Load Balancing Page
![image](https://github.com/user-attachments/assets/75a6492c-95d9-48c3-9159-2d26d118b090)

VPN Page
![image](https://github.com/user-attachments/assets/2e486a0a-d723-4527-9334-defcd7e3e080)

DNS filtering page 
![image](https://github.com/user-attachments/assets/b3fe0e17-3c77-4e91-9494-52d91da8afac)

AdBlock Page (Web filtering)
![image](https://github.com/user-attachments/assets/44280cab-8478-4d96-a470-040f524d48be)

Software page (Pakes installer)
![image](https://github.com/user-attachments/assets/55c09628-1217-4228-92e6-01731967101e)

Backup Page
![image](https://github.com/user-attachments/assets/a6436d74-1647-4e2c-b90a-191d5db09d29)

System logs page 
![image](https://github.com/user-attachments/assets/946df8d8-c21e-43d0-a4ef-7a49584faac2)

Channel analysis page 
![image](https://github.com/user-attachments/assets/d037af41-e8d2-4a7c-b05e-ac1a7b83ebfe)

Realtime graphs page
![image](https://github.com/user-attachments/assets/73672b85-fce8-4638-8153-e143fe9b4995)

Load balancing status page
![image](https://github.com/user-attachments/assets/85f2c5b8-2432-42c0-b511-c3a98eddaef6)



The Raspberry Pi 4 Model B was chosen for this project due to its performance and compatibility with OpenWRT.

🔌 USB Adapter Selection (RT5370 Chipset)
During implementation, a USB adapter with the RT5370 chipset was used to enhance wireless connectivity.

Why RT5370?
✅ Developed by Ralink Technology – Known for strong OpenWRT compatibility.
✅ Supports IEEE 802.11n – Ensures reliable and consistent wireless performance.
✅ Easy Configuration & Community Support – Well-integrated into the OpenWRT ecosystem.

By leveraging the RT5370 chipset, this setup ensures stable wireless connectivity, seamless OpenWRT integration, and effective IoT firewall management.

Network configuration
This project sets up OpenWRT on a Raspberry Pi 4 Model B for optimized network management, security, and connectivity.

🔧 Key Configurations
1️⃣ Core Network Settings
Loopback (loopback) – Assigns 127.0.0.1/8 for testing & troubleshooting.
IPv6 Prefix (ula_prefix) – Uses fd83:39e6:34ea::/48 for local network communication.
2️⃣ Network Interfaces
Bridge (br-lan) – Combines interfaces, with eth0 as the main port.
LAN (lan) – Configures br-lan with static IP 10.12.12.1/24 for internal networking.
Wireless WAN (wwan) – Operates in DHCP mode for dynamic IP allocation.
3️⃣ DNS & VPN
DNS Servers – Uses Cloudflare (1.1.1.1) & Google (8.8.8.8) for fast and reliable name resolution.
VPN Client (vpnclient) – Connects via tun0 to encrypt traffic and enhance security.
✅ Benefits
🚀 Optimized Traffic Management
🌍 Reliable Internal & External Connectivity
🔐 Enhanced Security with VPN Integration

![image](https://github.com/user-attachments/assets/ff518605-f41c-4bb0-8877-8862420306d9)

Wireless configuration

This setup enhances wireless security and network flexibility on OpenWRT by utilizing multiple wireless devices and interfaces to act as an IoT firewall.

🔐 Key Configurations
1️⃣ External Network Access
Connects to an external network for internet access.
2️⃣ USB Adapter (RT5370)
Establishes a secure access point (AP) for device connectivity.
3️⃣ Primary Wireless Device (radio0)
Channel: 7 (5GHz, HT20 mode) – Provides better speed & coverage.
Mode: Station Mode (sta) – Connects to an external SSID using WPA2 encryption.
4️⃣ Secondary Wireless Device (radio1)
Channel: 2 (2.4GHz, HT20 mode) – Enhances network flexibility.
Mode: Access Point (AP) –
Creates a WPA2-protected local network named "IoT Firewall".
✅ Benefits
🔒 Secure & Encrypted Connectivity
🌍 Dual-Band Wi-Fi for Flexibility
🛡️ Isolated Local Network for IoT Security

![image](https://github.com/user-attachments/assets/5fb44c5b-bbfb-4f39-bb49-62f63652714a)

Firewall configuration

This firewall setup secures network traffic while acting as an IoT firewall, protecting internal devices and ensuring stable connectivity.

🔐 Key Configurations
1️⃣ Default Security Measures
SYN Flood Protection – Prevents DoS attacks.
Traffic Policies –
Accepts incoming & outgoing traffic by default.
Rejects forwarded traffic for security.
2️⃣ Firewall Zones
LAN (lan) – Allows incoming, outgoing, and forwarded traffic for internal communication.
WAN (wan) –
Rejects incoming & forwarded traffic.
Allows outgoing traffic with NAT (masquerading) and MTU fixing.
VPN (vpn) –
Allows incoming & outgoing traffic.
Blocks forwarding to keep VPN traffic isolated.
3️⃣ Traffic Forwarding
LAN-to-WAN forwarding enabled, allowing internal devices to access the internet.
4️⃣ Essential Network Rules
Allows:
✅ DHCP renew
✅ ICMP ping
✅ IGMP (multicast)
✅ DHCPv6 & ICMPv6 for IPv6 support
✅ Benefits
🛡️ Enhanced Security – Protects against unauthorized access.
🚀 Stable Connectivity – Ensures reliable network operation.
🌍 IPv6 & Multicast Support – Improves future-proofing.


![image](https://github.com/user-attachments/assets/e76a813b-a1c9-4bc8-8f56-9100ded600dd)

![image](https://github.com/user-attachments/assets/6a864012-9f2e-4949-bdf5-a6721ca9192c)

VPN configuration

This setup integrates a VPN into OpenWRT on the Raspberry Pi 4 Model B, ensuring secure and private internet access through a customized configuration file.

📌 Key Configurations
Custom VPN Configuration (custom_config)
Uses /etc/openvpn/my-vpn.conf for custom VPN settings.
Disabled by default (option enabled '0') for flexibility in customization.
VPN Setup Requirements
Download the NordVPN Configuration File
Choose a server from: [NordVPN Server Tool](https://nordvpn.com/servers/tools/)
Upload the Config File to Raspberry Pi
scp your_file_name_here root@10.71.71.1:/etc/openvpn/client.conf
Apply Custom VPN Settings
Follow the instructions in raspberry_pi_nordvpn_config.txt.

🛠 Installation & Configuration
1️⃣ Install Required Packages
opkg update
opkg install luci-app-openvpn
/etc/init.d/rpcd restart
2️⃣ Configure VPN Parameters
OVPN_DIR="/etc/openvpn"
OVPN_ID="client"
OVPN_USER="USERNAME"
OVPN_PASS="PASSWORD"

# Save username/password credentials
umask go=
cat << EOF >${OVPN_DIR}/${OVPN_ID}.auth
${OVPN_USER}
${OVPN_PASS}
EOF
3️⃣ Configure VPN Service
# Update OpenVPN configuration
sed -i -e "
/^auth-user-pass/s/^/#/
/^redirect-gateway/s/^/#/
\$a auth-user-pass ${OVPN_ID}.auth
\$a redirect-gateway def1 ipv6
" ${OVPN_DIR}/${OVPN_ID}.conf

/etc/init.d/openvpn restart
4️⃣ Enable VPN Instance Management
ls /etc/openvpn/*.conf | while read -r OVPN_CONF
do
  OVPN_ID="$(basename ${OVPN_CONF%.*} | sed -e "s/\W/_/g")"
  uci -q delete openvpn.${OVPN_ID}
  uci set openvpn.${OVPN_ID}="openvpn"
  uci set openvpn.${OVPN_ID}.enabled="1"
  uci set openvpn.${OVPN_ID}.config="${OVPN_CONF}"
done

uci commit openvpn
/etc/init.d/openvpn restart
🔥 Firewall Configuration
uci rename firewall.@zone[0]="lan"
uci rename firewall.@zone[1]="wan"
uci del_list firewall.wan.device="tun+"
uci add_list firewall.wan.device="tun+"
uci commit firewall
/etc/init.d/firewall restart
🔄 Hotplug Configuration (Ensuring VPN Restarts on Reconnection)
mkdir -p /etc/hotplug.d/online

cat << "EOF" > /etc/hotplug.d/online/00-openvpn
/etc/init.d/openvpn restart
EOF

cat << "EOF" >> /etc/sysupgrade.conf
/etc/hotplug.d/online/00-openvpn
EOF

✅ Benefits
🔒 Secure & Private Internet Access
🚀 Customizable VPN Configuration
🔄 Auto-Reconnect on Connection Drops
🌍 IPv6 & Failover Support


![image](https://github.com/user-attachments/assets/c112ebe0-4e03-4317-8bc2-b29b694fb652)


DNS Filtering

This setup enhances DNS security and privacy on OpenWRT by encrypting DNS queries using DNS over HTTPS (DoH), preventing eavesdropping and interception.

🔐 Key Configurations
Canary Domains – Includes canary_domains_icloud and canary_domains_mozilla to verify DoH functionality.
Forced DNS Routing –
force_dns set to 1, ensuring all DNS traffic is encrypted.
Redirects ports 53 and 853 to the HTTPS DNS proxy.
🌍 DNS Resolver Settings
Google DNS
Bootstrap DNS: 8.8.8.8, 8.8.4.4
Resolver URL: https://dns.google/dns-query
Listening Address: 127.0.0.1:5054
Security: Runs as user 'nobody' and group 'nogroup'
AdGuard DNS
Bootstrap DNS: 94.140.14.14
Resolver URL: https://dns.adguard.com/dns-query
Listening Address: 127.0.0.1:5053
Logging: Enabled with verbosity level 1, logs stored at /var/log/https-dns-proxy.log
🛡️ Benefits
✅ Encrypted & Secure DNS Queries 🔒
✅ Prevents Unencrypted Requests 🚫
✅ Reliable & Backup DNS Resolution ⚡

![image](https://github.com/user-attachments/assets/18d59f97-0cb0-4980-82cd-1b93b292f798)

Web filtering 
This setup enhances network security and user experience on OpenWRT by blocking ads and malicious URLs, ensuring a cleaner and safer browsing environment.

🛠 Key Configurations
Global Settings (global)
Adblock Enabled: ✅ (adb_enabled '1')
Disabled Features:
Debugging (adb_debug '0')
Forced DNS (adb_forcedns '0')
SafeSearch (adb_safesearch '0')
DNS Filter Reset (adb_dnsfilereset '0')
Mail Reports (adb_mail '0')
General Reporting (adb_report '0')
Backup Enabled: ✅ (adb_backup '1') – Ensures configuration retention.
📡 Adblocking Sources
Adaway – Specializes in mobile ad blocking.
AdGuard – Comprehensive blocking across multiple platforms.
Disconnect – Prevents tracking & privacy breaches.
Yoyo – Blocks general ad domains effectively.
⚙ DNS & Fetch Utility
DNS Resolver: dnsmasq – A fast DNS forwarder and DHCP server that integrates with Adblock.
Fetch Utility: uclient-fetch – A lightweight HTTP client for updating blocklists.
✅ Benefits
🚀 Faster Browsing – Blocks unwanted ads & trackers.
🔐 Improved Security – Prevents access to malicious domains.
📡 Better Privacy – Reduces tracking & unwanted content.

![image](https://github.com/user-attachments/assets/9d635fd1-662a-415c-851f-9574dca4c001)

Load Balancing configuration
This setup utilizes MWAN3 to manage multiple WAN interfaces in OpenWRT, providing load balancing and failover support for enhanced network reliability.

⚙ Key Configurations
Global Settings (globals)
Defines a monitoring mask to track multiple WAN interfaces.
IPv4 WAN Interfaces (wan & wanb)
Tracking IPs: 1.1.1.1 (Cloudflare) & 8.8.8.8 (Google).
Dependability Metric: 2 – Indicates importance in load balancing.
IPv6 WAN Interfaces (wan6 & wanb6)
Tracking IPs:
2606:4700:4700::1111 (Cloudflare).
2620:0:ccc::2 (Google).
Load Balancing & Failover Support – Ensures IPv6 network stability.
✅ Benefits
🔄 Seamless Failover – Automatically switches between WAN connections.
⚡ Load Balancing – Distributes traffic across multiple WANs for better performance.
🔗 Improved Network Stability – Tracks multiple ISPs for redundancy.

![image](https://github.com/user-attachments/assets/23de373f-228d-4236-b86b-07deb89ed44b)

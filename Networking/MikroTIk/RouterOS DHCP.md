#### Access DHCP Server Settings:

- Open WinBox and connect to your MikroTik router.
- Navigate to "IP" > "DHCP Server."

#### DHCP Server Configuration:

- Click on the "+" button to add a new DHCP server.
- Enter a name for the DHCP server (e.g., "dhcp1").
- Choose the interface where the DHCP server will run.
- Set the Address Pool (IP range) for dynamic IP assignment.

#### Network Configuration:

- Specify the network settings:
    - `Address Pool`: Set the range of IP addresses to be assigned.
    - `Gateway`: Enter the IP address of your router.
    - `DNS Servers`: Optionally, specify DNS server addresses.
    - `WINS Servers`: Optionally, specify WINS server addresses.
    - `Domain`: Enter the domain name for your network.

#### Lease Time:

- Set the lease time for IP addresses. This determines how long an assigned IP address is valid. Shorter lease times can be useful in dynamic environments.

#### DHCP Options:

- You can configure additional DHCP options if needed (e.g., default route, NTP servers, etc.).

#### Networks Tab:

- In the "Networks" tab, configure the DHCP server to listen on specific interfaces.
- Enable the DHCP server on the desired interfaces.

#### Apply Changes:

- Click "Apply" or "OK" to save the DHCP server configuration.

#### DHCP Client Configuration (if needed):

- If your MikroTik router is receiving its IP address dynamically from an upstream DHCP server, you can configure the DHCP client settings in "IP" > "DHCP Client."

#### Monitor DHCP Leases:

- Go to "IP" > "DHCP Server" > "Leases" to view active DHCP leases.

#### Troubleshooting:

- If devices are not receiving IP addresses, ensure the DHCP server is enabled, the address pool is configured correctly, and there are no conflicts with statically assigned IPs.

#### DHCP Relay (if needed):

- If your network spans multiple subnets, consider configuring DHCP relay on routers to ensure DHCP requests reach the DHCP server.
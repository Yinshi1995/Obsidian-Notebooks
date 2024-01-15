#### Access RouterOS CLI

- Open a terminal or SSH client to connect to your MikroTik router.

#### Basic Commands

- **`/interface print`**: List all interfaces.
- **`/ip address print`**: Show IP addresses.
- **`/ip route print`**: Display routing table.
- **`/system resource print`**: Show system resources.

#### Configuration Commands

- **`/interface set [interface] [property=value]`**: Configure interface properties.
- **`/ip address add address=x.x.x.x/xx interface=[interface]`**: Add IP address.
- **`/ip route add dst-address=0.0.0.0/0 gateway=x.x.x.x`**: Add default route.
- **`/system identity set name=[name]`**: Set router identity.

#### Firewall Commands

- **`/ip firewall filter print`**: Display firewall filter rules.
- **`/ip firewall nat print`**: Show NAT rules.
- **`/ip firewall address-list print`**: List address lists.

#### DHCP Server Commands

- **`/ip dhcp-server print`**: Show DHCP server settings.
- **`/ip dhcp-server lease print`**: Display DHCP leases.

#### Wireless Commands

- **`/interface wireless print`**: Show wireless interfaces.
- **`/interface wireless set [interface] [property=value]`**: Configure wireless interface.

#### VPN Commands

- **`/ip ipsec peer print`**: Display IPSec peers.
- **`/interface pptp-server server print`**: Show PPTP server settings.
- **`/ip pool print`**: Display IP address pools.

#### Monitoring Commands

- **`/system resource print`**: Display resource usage.
- **`/interface monitor-traffic [interface]`**: Monitor traffic on an interface.
- **`/tool bandwidth-test [address]`**: Perform bandwidth test.

#### Scripting

- **`/system script print`**: Show scripts.
- **`/system script run [script-name]`**: Run a script.

#### Batch Execution

- **`/system script add name=batch-script source={"command1" "command2"}`**: Create a script with multiple commands.
- **`/system script run batch-script`**: Run the batch script.

#### File Management

- **`/file print`**: List files.
- **`/file remove [file-name]`**: Delete a file.
- **`/file get [file-name] contents`**: Display file contents.

#### Save Configuration

- **`/export file=config-backup`**: Export configuration to a file.
- **`/import file=config-backup`**: Import configuration from a file.

#### Exit

- **`/quit`**: Exit the RouterOS CLI.
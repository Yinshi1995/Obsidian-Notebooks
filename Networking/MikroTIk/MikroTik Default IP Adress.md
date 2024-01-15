MikroTik RouterOS devices typically have default IP addresses assigned to their interfaces for initial configuration. Here are the common default IP addresses used by MikroTik routers:

1. **Default IP for Ethernet Interfaces:**
    
    - The default IP address for the Ethernet interfaces on a MikroTik router is often set to `192.168.88.1`. You can connect to the router using this IP address to access the web-based configuration interface.
2. **Default IP for Wireless Interfaces:**
    
    - For wireless interfaces, the default IP address is also commonly set to `192.168.88.1`. This is the IP address you would use to configure the router's wireless settings.
3. **Default IP for Loopback Interface:**
    
    - MikroTik routers might also have a default IP address set on the loopback interface, commonly `127.0.0.1`. This IP address is used for internal routing and communication within the router itself.
4. **Default IP for Other Interfaces:**
    
    - In addition to Ethernet and wireless interfaces, MikroTik routers may have other types of interfaces (e.g., SFP, LTE, etc.). The default IP addresses for these interfaces can vary, but `192.168.88.1` is a common default.
5. **DHCP Client for WAN Interface:**
    
    - If the router is configured to obtain an IP address dynamically from an upstream provider (such as an ISP), the WAN interface might use DHCP. In this case, the router will receive an IP address automatically from the ISP.

It's important to note that these default IP addresses are set for initial configuration and are commonly used out of the box. However, they can be changed during the configuration process to suit the specific needs of the network. When connecting to a MikroTik router for the first time, it's a good practice to check the documentation or any labels on the device for the default IP address information.

Additionally, the MikroTik WinBox utility allows you to discover MikroTik devices on your network even if their IP addresses have been changed. You can connect to them using their MAC addresses or other identifying information.
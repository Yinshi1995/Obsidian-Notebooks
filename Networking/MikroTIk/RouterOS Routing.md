#### Access Routing Configuration

- Open WinBox and connect to your MikroTik router.
- Navigate to "IP" > "Routes."

#### Add Static Route

- Click on the "+" button to add a new static route.
- Enter the destination network and gateway address.
- Set the target interface for the route.

#### Dynamic Routing Protocols

- If using dynamic routing protocols:
    - Go to "IP" > "Routes."
    - Enable OSPF, BGP, or other routing protocols.
    - Configure protocol-specific settings.

#### OSPF Configuration

- For OSPF (Open Shortest Path First):
    - Navigate to "Routing" > "OSPF."
    - Add OSPF instances and configure area settings.
    - Assign networks to OSPF areas.

#### BGP Configuration

- For BGP (Border Gateway Protocol):
    - Navigate to "Routing" > "BGP."
    - Add BGP instances and configure AS (Autonomous System) settings.
    - Establish BGP peerings and exchange route information.

#### Policy-Based Routing

- Implement Policy-Based Routing if needed:
    - Go to "IP" > "Firewall" > "Mangle."
    - Add mangle rules to mark packets.
    - Create routing rules based on marked packets.

#### Default Route Configuration

- Configure the default route:
    - Go to "IP" > "Routes."
    - Add a default route with the gateway address.

#### Monitoring Routes

- Monitor active routes in "IP" > "Routes."
- Use the "Routing" > "Route" menu for a detailed view.

#### Troubleshooting

- Check routing tables and ensure correct route entries.
- Verify dynamic routing protocol configurations.
- Use tools like traceroute for network diagnostics.

#### Adjusting Routing Metrics

- Fine-tune routing metrics for dynamic routing protocols.
- Adjust administrative distances and metrics for static routes.

#### Apply Changes

- After configuring routing settings, click "Apply" or "OK" to save changes.
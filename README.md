# Network-Configuration
## What's configured
- OSPF (Process 110) across all routers for internal routing
- BGP (AS 65001 ↔ 65002 ↔ 65003) for inter-AS routing
- GRE Tunnel between Edge-Router-HQ and Edge-Router-Site
- ACL 150 — blocks ICMP from 211.0.1.1
- ACL TUNNEL_IN — blocks ICMP through tunnel interface
- DHCP relay (ip helper-address) on site router
- Syslog configured on a server

I have used gre tunnel to make the edge router act as neighbor and thus share ospf information
and know the network topology of each site 

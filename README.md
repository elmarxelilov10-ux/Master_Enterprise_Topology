# Master_Enterprise_Topology
## Progress of my master project
I am building this master topology because i realized that in real life engineer rarely build infrastructure from 0 but integrate concepts. So i decided to build one master project and integrate concepts i learn to it.
## Topology overview:
* I have double of every roles in topology from access to edge for HA.
* I have put 2 Access switches for users to connect and 2 Cores . They both are L2 switches and only responsible for L2.
* Then i have 2 PaloAlto's which monitors and routes packets of project.
* I also have put OutOfBand management network so remote employees can connect and also if internal devices don't respond ,IT workers connect through OOB.
* I used /31 subnets for point-to-point devices and maximumly no waste IPs.
## Phase 1 Internal connectivity: 8/12/26
 * Initial config
 * Vlans can reach each other through subinterfeces of Palo
 * Loopback of devices
 * Out of Band management
## Phase 2 Basic Internal security
* configuring HA on both PaloAlto FWs. HA need two links one for control and other for data (sync configs).
* Configured DMZ zone interface on PaloAlto and also configured IP of ubuntu which will serve as public server in future.
* Did device hardening with my prewritten switch hardening file + L2 security
* and lastly configured ACL for ssh so only IT vlan can ssh devices.
## Phase 3 Outside Connectivity
* Configured eBGP with edge routers and ISP routers. AS 100 , AS 200 , AS 65000 .
* Configured iBGP between edge routers. AS 6500 . Wasn't necessary but did it for practice.
* Configured OSPF between FWs and edge routers.
* Used Loopback interfaces for all peerings . BGP made a problem and fixed by update source . And in eBGP i changed ttl to 3 because of loopbacks.
## Phase 4 NSE4 lesson 1-2
* Configured inital configs on both Fortigates
* DHCP server in port1
* ip helper-address in OOB router
* created two VPN profiles 1 for full access other only read
* AND lastly logs in fortigate can be stored in two ways local and remote . Logs may be stored raw (archiving) and in SQL database (for analysis). Logs may be divided into 3 categories Traffic Logs (Data plane) ,Event Logs (Management and system Plane) and Security Logs.
## Phase 5 NSE4 lesson 3-4
*FortiGate Policies: Configured test policies to practice them.
 *Policy NATs : in OBB-FrotiG-01 i used policy NATs to configure NAT individually for each policy.
 *CNAT : in OBB-FrotiG-02 i used central NAT to centralize the NAT processes.
 *Features enabling : enabled multiple interfaces and unnamed policies features.
 *Security Profiles : enabled security profiles in policies to study them.


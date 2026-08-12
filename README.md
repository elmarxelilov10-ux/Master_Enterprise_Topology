# Master_Enterprise_Topology
## Progress of my master project
I am building this master topology because i realized that in real life engineer rarely build infrastructure from 0 but integrate concepts. So i decided to build one master project and integrate concepts i learn to it.
## Topology overview:
* **I have double of every roles in topology from access to edge for HA.I have put 2 Access switches for users to connect and 2 Cores . They both are L2 switches and only responsible for L2. Then i have 2 PaloAlto's which monitors and routes packets of project. I also have put OutOfBand management network so remote employees can connect and also if internal devices don't respond ,IT workers connect through OOB. I used /31 subnets for point-to-point devices and maximumly no waste IPs.
## Phase 1 Internal connectivity: 8/12/26
 * Initial config
 *Vlans can reach each other through subinterfeces of Palo
 * Loopback of devices
 * Out of Band management

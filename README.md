# FinalProjectCNIT381
ssh-keygen -f "/home/devasc/.ssh/known_hosts" -R "10.1.1.1"

Students:Connor Simon, Zach Koski, Brendan Pryor

**Overview**
These ansible playbooks represent the convience and power of network automation. Within these 6 playbooks you get the configurations for inital configurations (IP addresses, interface descriptions, banner, etc.), VLANs, EIGRP dynamic routing, NTP, as well as connectivity testing. A playbook for backup file creation also included. this playbook with capture and create a backup file of the devices running configurations, and VLAN briefs with easy to identify naming schemes.


**Project Structure**

├── README.md

├── ansible.cfg

├── inventory.ini

├── playbooks/

│ ├── 01_verify_connectivity.yml

│ ├── 02_base_config.yml

│ ├── 03_eigrp_config.yml

│ ├── 04_vlan_config.yml

│ ├── 05_services_config.yml

│ └── 06_backup_config.yml

  └── documentation/

   ├──Addressing Table
    
   ├──Topology
  
   └── VLANs

**Playbooks**
Verify connectivity: verifies the connectivity between all the devices on the network.
Command: ansible-playbook playbooks/01_verify_connectivity.yml

Base Configuration: Configures hostnames, interface descriptions, and IP addresses.
Command: ansible-playbook playbooks/02_base_config.yml

EIGRP: Configures three loopback interfaces per router, EIGRP AS 100, and the network advertisements.
Command: ansible-playbook playbooks/03_eigrp_config.yml

VLAN config: Congigures VLANS and trunk port toward the routers. 
Command:ansible-playbook playbooks/04_vlan_config.yml

Services: Configures NTP and logging.
Command:ansible-playbook playbooks/05_services_config.yml

Backup config: Saves running configs to the directory
Command: ansible-playbook playbooks/06_backup_config.yml


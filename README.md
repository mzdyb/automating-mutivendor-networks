# Automating multivendor networks with Ansible Automation Platform
This project shows the concept of managing multivendor network environment with Event Driven Ansible for events triggering and NetBox as CMDB for network configuration.
There are three workflows implemented here:
1. Populate NetBox with network devices and the required objects (Sites, Manufacturers, Device Types, Device Roles)
2. Automatically push a subset of devices' configuration changes (vlan database, IP address) to NetBox:  
   CLI change -> syslog-ng server -> (webhook) -> Event-Driven Ansible rulebook -> Ansible Automation Platform -> NetBox
3. Automatically push a change performed on NetBox (IP address change on interface) to devices configuration:  
   Change on NetBox -> (webhook) -> Event-Driven Ansible rulebook -> Ansible Automation Platform -> network device configuration

The following network topology simulated on EVE-NG is used for this project:
![multivendor_topo](https://github.com/mzdyb/automating-mutivendor-networks/assets/49950423/19c3e0db-d3a4-4948-aab6-3b52c3541a5b)  


The project is based on the concept described in details in the following youtube video:  
https://youtu.be/qhoaTd8RDNk?si=bEk4Ho7v4RGnLcKJ

## Feedback
Feedback is always welcome! If you have any comments, please reach me out

## Author

[@mzdyb](https://www.linkedin.com/in/michal-zdyb-9aa4046/)

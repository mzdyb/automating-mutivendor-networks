# Automating multivendor networks with Ansible Automation Platform
This project shows the concept of managing multivendor network environment with Event Driven Ansible for events triggering and NetBox as CMDB for network configuration.
There are three workflows implemented here:
1. Populate NetBox with network devices and the required objects (Sites, Manufacturers, Device Types, Device Roles)
2. Automatically push a subset of devices' configuration changes (vlan database, IP address) to NetBox  
   CLI change -> syslog-ng server -> (webhook) -> Event-Driven Ansible rulebook -> Ansible Automation Platform -> NetBox
3. Automatically push a change performed on NetBox (IP address change on interface) to devices configuration  
   Change on NetBox -> (webhook) -> Event-Driven Ansible rulebook -> Ansible Automation Platform -> network device configuration

# Deploying challenge VMs

The Ansible playbooks in this repository make deploying VMs for your CTF challenges simple and quick, just follow these steps:

  1. Create as many instances as you need to run your challenges using Ubuntu 16.04 images.
 
  2. Get the IPs of the instances you just created (e.g. `openstack server list`) and add them to the `inventory` file, following the template used previously in it.
  
  3. Run the playbooks:
    - `ansible-playbook vpn_base_container.yml`
    - `ansible-playbook vpn_host.yml`
    - `ansible-playbook challenges.yml`
    
  They will set the VPN and the Challenges' containers with their required packages and settings, and you should be ready to go configure the [provisioner](https://github.com/pwn2winctf/NIZKCTF-provisioning) if you haven't done that yet.

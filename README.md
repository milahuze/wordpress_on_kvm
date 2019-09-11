# wordpress_on_kvm
1. Ansible repository is supposed to work from hypervisor machine which is stated as 127.0.0.1 in repo. It is supposed that Debian is installed on hypervisor.
2. To create guest VMs with static IPs, their IPs should be added to group 'guest' in hosts file and playbook should be executed:
* ansible-playbook start_guests.yml
Please note that stopping of guests and releasing IP addresses were not implemented as not requested in task.
3. To install wordpress and all related software to guest VMs, please, run:
* ansible-playbook setup_wordpress.yml
4. To install NGINX on hypervisor as balancer to guest VMs wordpress instances:
* ansible-playbook setup_nginx.yml
5. To install security updates on guest VMs:
* ansible-playbook install_securityupdates.yml
6. To configure IPTABLES on guest VMs: *under construction*




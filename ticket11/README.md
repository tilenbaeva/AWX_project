# TICKET 11 #

Made all the previous playbooks interactive.
Each playbook has a comments section on top, where it explains which variable should be given when prompted during a template launch on ansible tower

Example from route53.yaml:

- Please specify the following variables when prompted while launching the template   
- state: present | absent | get | create | delete 
- zone: The DNS zone to modify, e.g. example.com
- record: The full DNS record to create or delete e.g. tower.example.com
- type: A | CNAME | MX | AAAA | TXT | PTR | SRV | SPF | CAA | NS | SOA
- ttl: The TTL to give the new record
- value: The new value when creating a DNS record

Playbooks:
- "start_service.yaml " ==> installs LAMP on CentOS7 and start services
    - by using this template you can install any services and start

- "stop_sservices.yaml" ==> this playbook  stops LAMP services on CentOS7
    - by using this template you can start, restart, stop, enable any services

- "ssh.yaml"            ==> creates user with ssh key to remote hosts
    - in this playbook I am creating user "bob" with ssh key generated

- "copy_ssh.yaml"       ==> creates user with ssh key and gets it's ssh key to authorized keys of another systems
    - this playbook will take user "bob's" ssh public key and copy to root's home directery in authorized_key (path: /root/authorized_key) in another remote hosts

            - - - to be continued - - - 
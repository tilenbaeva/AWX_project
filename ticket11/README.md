# TICKET 11 #

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
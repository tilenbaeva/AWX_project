#               AWX_project
* In this Anible AWX project we will have one inctance on any cloud provider services. 
* AWX tower will hosts, Linux distributions and Windows instances. 
************** In my case all my instances are on AWS *******************

- This repository inscludes different kind of playbooks -

###             How to install Ansible AWX 

I will be using 5 servers:  
            1.instance for Ansible AWX
            2. CentOS 7 
            3. Ubuntu 16.04
            4. Debian8/9 
                        with  minimal installation and SELinux in permissive mode.

192.168.1.25 AWX Server
192.168.1.21 host1
192.168.1.22 host2
192.168.1.23 host3
192.168.1.24 host4

#####   Minimum System Requirements for AWX Server
>> At least 4GB of memory
>>At least 2 cpu cores
>>At least 20GB of space
>>Running Docker, Openshift, or Kubernetes
>> Check the SELinux configuration.

#####   Tower Installation   
>> yum install -y epel-release 
>> yum install -y yum-utils device-mapper-persistent-data lvm2 ansible git python-devel python-pip python-docker-py vim-enhanced 
>> yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo 
>> yum install docker-ce -y 
>> systemctl start docker 
>> systemctl enable docker 
>> git clone https://github.com/ansible/awx.git 
>> cd awx  
>> git clone https://github.com/ansible/awx-logos.git 
>> cd installer/ 
>> vim inventory   # change below lines in conf.file
    postgres_data_dir=/var/lib/pgdocker 
    awx_official=true 
    project_data_dir=/var/lib/awx/projects 
>> ansible-playbook -i inventory install.yml -vv 
>> docker container ls
  # P.S. https://www.howtoforge.com/tutorial/centos-ansible-awx-installation/


  # THEN
   - Create AWX Organization
   - Setting up Git repo
   - Add AWS Users and Teams
   - AWX Access key and secret 
   - AWX adding private and public keys
        - above 2 steps are for (exchange them with hosts, so AWX server can talk/ping with./hosts)
   - Set up AWX local git
   - Set up AWX inventory
   - Ping/ add hosts, run ping.yaml playbook
   - Add Tenplate jobs to run playbooks
 
Two playbooks created to ping hosts in Ansible AWX

    * ping.yaml --> playbook will ping linux instances
    * win_ping.yaml --> playbook will ping windows instances.

* Every folder will have README.md
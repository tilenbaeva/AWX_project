### README PLEASE ###

* packages.yaml         -->  install vim on CentOS7, Ubuntu and Debian
                        install tree and telnet on CentOS7, Ubuntu and Debian

* archive90days.yaml    --> find files in /tmp that are older than 90 days and zip them (Linux Machines)

* archive2GB.yaml       --> find and zip files that are over 2GB (Linux Machines)

# NOTE: 
- If you created and installed instances recently for AWX project, so then you will not have file that 90 days older, over or 2GB. To able to run this playbooks and check if they are working, run below playbook:

* createfiles.yaml      --> this playbook will create files that are bigger than 2GB. 

# NOTE: 
- After testing all playbooks make sure you run deletefiles.yaml that will delete your files created by another playbook. 


                    ### END  ####
                  ### but not end ####


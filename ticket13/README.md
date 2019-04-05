This playbook is template to take backup of DB folder. Playbook will require 4 inout from user.

1. IP of the DB host
2. DB folder location  (usually /var/lib/mysql)

3. IP of the Backup server (can be just linux machine different from DB) 
4. /backups folder (can be any location.)


User should be able to execute and take a backup of DB and send the backup to another host. Playbook should zip first and send the zipped backup folder across the internet


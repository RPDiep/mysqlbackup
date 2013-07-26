mysqlbackup 
=========== 
 
A script to create mysql backups and keep backups with a retention scheme.  
It creates backups every 15 minutes and every three hours a backup with Percona XtraBackup.  
 

## Requirements: ##
*  [Percona XtraBackup] (http://www.percona.com/software/percona-xtrabackup).  


## Installation: ##

1.  Create a .my.cnf file with mysql root credentials in /root:

        [client]
        user     = <mysql-root-user>
        password = <password>

2.  Install the script as /usr/local/sbin/backup
3.  Setup a cron job:  

        */15 * * * * /usr/local/sbin/backup
 
 
## Retention scheme: ##
 
*   12 monthly backups are maintained 
*   4 weekly backups 
*   7 daily backups 
*   96 backups of every 6 hours 
*   48 backups of every 3 hours 
*   96 quarterly backups 


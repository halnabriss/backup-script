# backup-script
Bash script to create full and incremental backups for Linux files
This script is created by Hadi Alnabriss (alnabris@gmail.com)
It can be freely used, modified and redistributed
The script makes Full and incremental backups for your data, in the default configurations it creates a full backup every Sunday, and incremental backups on the other days of the week.
You should customize the variables in the script accoridng to your needs:
1. Which data you want to backup (Backup_Data=" /var/www/ /etc/httpd/conf.d/")
2. When do you want to male your full backups (Full_Backup_Day=0) 0 for sunday.
3. Backup Device, in this example I'm using an external disk (Backup_Dev=/dev/nvme0n2)
4. Backup Location, in the example I'm using /mnt/backup (Backup_Dir=/mnt/backup/)
5. Full backup Size , In this example we assume that full backup requires 5GB (Full_Backup_Size=5000000)
6. Incremental Backup Size, In the script we assume that we need 1GB for each incremental backup (Inc_Backup_Size=1000000)

We also use the file /var/log/backup_script as a logging file for our script important logs.

# Linux

### SSL
- https://www.youtube.com/watch?v=BTm47R7_Wdk
- https://letsencrypt.org/docs/
- https://www.cyberciti.biz/faq/how-to-forcefully-renew-lets-encrypt-certificate/ - Renew
    - Make sure your domain can be pinged on http for the moment it needs to be renewed

### Tips
- SERVERS ON ARE UTC TIME SO THEY ARE 4 HOURS AHEAD
```
sudo timedatectl set-timezone UTC
```

### linux file system
- https://www.howtogeek.com/117435/htg-explains-the-linux-directory-structure-explained/#:~:text=%2Fetc%20%E2%80%93%20Configuration%20Files,in%20each%20user's%20home%20directory.

### set permanent environment variables
- https://www.serverlab.ca/tutorials/linux/administration-linux/how-to-set-environment-variables-in-linux/

### Systemd
- https://www.digitalocean.com/community/tutorials/understanding-systemd-units-and-unit-files
- https://www.digitalocean.com/community/tutorials/how-to-use-systemctl-to-manage-systemd-services-and-units
- use systemd
```
sudo systemctl start application
stop
reload (if you want to be able to reload without restarting in the case of a change in config files)
restart
enable - enables a service at boot (if you want to start it, either run the start command or restart the server)
disable - disables from starting automatically
status - checks status
is-enabled - see if service is enabled
is-failed
is-active
```

### Add directory to path
- https://linuxize.com/post/how-to-add-directory-to-path-in-linux/

### Journalctl
- https://www.digitalocean.com/community/tutorials/how-to-use-journalctl-to-view-and-manipulate-systemd-logs

### Functions
- https://www.geeksforgeeks.org/function-command-in-linux-with-examples/

### Environment variables
```
export NAME=VALUE (to set)
echo $NAME (to check the value )
unset NAME (unset)
set NAME (check all environment variables)
```

### Commands
- Delete git repo 
```
 -rm -rf .git
```
- Push to master
```
git push origin master
```
- switch to root
```
sudo su - 
passwd ubuntu
```
- See file permissions
```
ls -l
```
- see all files
```
ls -a
```
- execute a command as user other than root
```
-u
```
- list processes
```
ps
```
- List everything
```
ps -e
```
- List all processes with more info
```
ps -ef
```
- exit foreground process
```
ctrl + c
```
- suspend foreground process
```
ctrl + z
```

## Logging

- https://www.digitalocean.com/community/tutorials/how-to-manage-logfiles-with-logrotate-on-ubuntu-16-04
- https://www.networkworld.com/article/3538471/how-to-compress-files-on-linux-5-ways.html
- https://www.tecmint.com/install-logrotate-to-manage-log-rotation-in-linux/
- https://www.havetheknowhow.com/Configure-the-server/Install-ssmtp.html
- https://vitux.com/three-ways-to-send-email-from-ubuntu-command-line/

### Stderr
- https://linuxize.com/post/bash-redirect-stderr-stdout/
- https://www.cyberciti.biz/faq/redirecting-stderr-to-stdout/

### Cloudwatch logs
- https://wellarchitectedlabs.com/security/200_labs/200_remote_configuration_installation_and_viewing_cloudwatch_logs/4_start_cw_agent/
- https://www.youtube.com/watch?v=mw_-0iCVpUc - upload to S3

## Redis

### CLI
```
sudo apt-get install redis-tools
redis-cli -h developmentredis.wo3pya.0001.use1.cache.amazonaws.com -p 6379
```

## PostgreSQL
```
psql --host=database-1.cxjgs3gfrmni.us-east-1.rds.amazonaws.com --port=5432 --username=postgres --password --dbname=master

install postgres client
sudo apt-get update
sudo apt-get install postgresql-client

```

## Ubuntu

### Update
```
sudo apt update 
sudo apt upgrade 
sudo apt full-upgrade
sudo reboot
sudo apt autoremove

```

## NGINX

- NGINX log is in ```var/log```
- Check nginx
```
Systemctl status nginx
```
- NGINX Commands
```
sudo systemctl stop nginx
sudo systemctl start nginx
sudo systemctl restart nginx
sudo systemctl reload nginx (If you are only making config changes, Nginx can often reload without dropping connections if you do this command)
sudo systemctl disable nginx
stops automatic start when server boots
sudo systemctl start nginx (enable nginx to start when the server boots (if it is not enabled already))
sudo nginx -t (test configuration files)
```

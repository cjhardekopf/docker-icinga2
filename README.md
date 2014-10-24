docker-icinga2
==============

Icinga2 and icinga-web using /data for configuration. The icinga2 configuration (usually in /etc/icinga2) will be in /data/icinga2. The only part to be configured dynamically is the MySQL database connection as json in the "icinga2/mysql" key as follows:
* user - Database user
* password - Database password
* host - Database host
* database - Database name

The icinga-web configuration is json in the "icinga2/web-mysql" key ad follows:
* user - Database user
* password - Database password
* host - Database host
* database - Database name

In addition, mail needs to be configures using a json key "msmtp" as follows:
* tls - If set to either "starttls" or "nostarttls" then use tls with 
    starttls either on or off
* host - Mail host
* port - Mail port (defaults to 25)
* from - Either a from mail address or "auto"
* maildomain - mail domain when using auto_from
* logfile - Log file to use
 

# Linux Server Configuration Project

### About
This project is about having  baseline installation of a Linux distribution on a virtual machine and preparing it to host web applications, including installing updates, securing it from a number of attack vectors and installing/configuring web and database servers.

### How to access
SSH Port: 2200
Public IP Address: 52.36.234.235
URL of hosted web application: http://ec2-52-36-234-235.us-west-2.compute.amazonaws.com
Sudo password is Udacity_Grader

### Summary of configurations done

1. Created a new user named 'grader'.
2. User 'grader' is granted sudo permissions.
3. Remote login for 'root' user is disabled.
4. Set a password for user 'grader'.
5. Key-based SSH authentication is enforced.
6. SSH is hosted on a non-default port.
7. The firewall has been configured to monitor for repeated unsuccessful ssh logins and bans attackers.
8. All currently installed packages are updated.
9. Local timezone is configured to UTC.
10. A cron job is written to automatically run packag updates on a weekly basis.
11. Uncomplicated Firewall (UFW) is configured to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123)
12. Apache installed and configured to serve a Python mod_wsgi application
13. PostgreSQL is installed and remote connections to PostgreSQL are now allowed.
14. A PostreSQL user 'catalog' is created and granted all privileges on database 'events_catalog'.
15. EventsCatalog application (https://github.com/mohammedsafwat/events-catalog) is deployed and can be accessed from this URL (http://ec2-52-36-234-235.us-west-2.compute.amazonaws.com)
16. Apache status monitoring is configured using Munin. You can access Munin from (http://ec2-52-36-234-235.us-west-2.compute.amazonaws.com/munin) 

### Pacakges installed

1. fail2ban
2. cron-apt
3. apache2
4. postgresql
5. postgresql-contrib
6. git
7. libapache2-mod-wsgi 
8. python-dev
9. python-pip
10. Flask
11. sqlalchemy
12. oauth2client
13. dict2xml
14. httplib2
15. google_api_python_client
16. Requests
17. flask-seasurf 
18. munin

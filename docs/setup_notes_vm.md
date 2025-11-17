# Setup for VM MySQL
## VM creation
1. Select instance to create.
2. Choose E2 for price and usability.
3. Choose e2-small for minimum of 2GB of memory.
4. Choose Ubuntu OS system.
5. Everything else kept to default.

## Firewall configuration
1. Create a firewall rule.
2. Name it and give it a description.
3. Set IP range to 0.0.0.0/0 to allow all IPs.
4. Set protocol to tcp:3306

## SSH steps
1. Input `sudo apt-get update` to update the OS system.
2. Input `sudo apt install mysql-server mysql-client` to install mysql into the server.
3. Input `sudo mysql` to log in into mysql.
4. Input `CREATE USER 'xxx'@'%' IDENTIFIED BY 'xxx';` to add user to database
5. Input `GRANT ALL PRIVILEGES ON *.* TO 'xxx'@'%' WITH GRANT OPTION;` to give all privileges to the user.
6. Edit mysqld.cnf file and input `0.0.0.0/0` to allow for other network connections.
7. Researt SSH and input `mysql -u xxx -p` to locally test the user connection to mysql.
8. Input the password you set to the username.

## Time to setup
1. It took roughly 30 minutes for VM creation and configuration, set up of VM MySQL, running the python script, and running a query within the VM.
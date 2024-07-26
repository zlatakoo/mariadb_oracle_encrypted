# mariadb_oracle_encrypted

(change Vagrant box mode from NAT to Bridge)

### 1. Install Oracle Linux throug vagrant box 
### 2. Install MariaDB with 
'''sudo yum install -y mariadb-server'''
### 3. Enable port 3300 in firewall with commands: 

### 4. Enable port 3300/tcp in SELinux with command:
'''sudo /usr/sbin/semanage port -a -t mysqld_port_t -p tcp 3300''

### 5. Edit /etc/my.cnf:
'''
[mysqld]
bind-address=192.168.50.234
port=3300
'''

### 6. Restart maridb service


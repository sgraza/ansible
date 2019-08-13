# Ansible Configuration

Software management configuration using ansible.

Operation System: Red Hat Enterprise Linux 8

Softwares:

1. Apache webserver
2. Tomcat application server
3. MySQL database server
4. Telnet
5. Curl
6. Nslookup
7. Oracle JDK

# Prerequisite

Choose where to install ansbile, it can be either from your:
1. remotely on your laptop (your own choice of OS)
2. locally on the ec2 instance created.

# To test connection to the hosts

Update the IP address in the hosts file

```
ansible kp_devops -i hosts -m ping
```

# Configure ansible on the following software:

Apache:

```
ansible-playbook -i hosts apache.yml
```

Mysql:

```
ansible-playbook -i hosts mysql.yml
```

Tomcat:

```
ansible-playbook -i hosts tomcat.yml
```

Common (curl,telnet,Oracle JDK and Nslookup):

```
ansible-playbook -i hosts common.yml
```

# Single Step Configuration

```
ansible-playbook -i hosts site.yml
```

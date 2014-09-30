### Ansible Playbook to automate the setup of an rsyslog server on AWS ec2 with EBS ###

### Preparation
1. Add the address of target host in hosts file

### Objective
#### This playbook will setup and gave to you an fully functional rsyslog central server.

### TODO

1. After install server, create an file on **"/etc/rsyslog.d/remote.conf"** with this content on clients:

```
##############################
*.* @TargetServerIpAddress:514
##############################
```
> PS: Don't forget to change "TargetServerIpAddress" by the real Ip Address
>> PS2: To apply changes on clients, remember to restart process, sometimes it don't work's with restart so be evil and "pkill -9 rsyslog"
### Credits

[Ansible Logstash Playbook](https://plus.google.com/+ValentinoGagliardi?rel=author)
[Ansible](http://www.ansible.com/)
[Rsyslog](http://www.rsyslog.com/)

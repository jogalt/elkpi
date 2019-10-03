ELKpi
=====

This is an ansible playbook for installing an ELK stack on Raspberry pi 2 or 3 or 4
Please change the values in vars-rpi.yml then launch with the following command; 

ansible-playbook -i hosts elk-rpi.yml

or, if your RPI requires password auth, this additional command will allow you to pass those values after the playbook starts.

ansible-playbook -i hosts  -v -b -c paramiko --ask-pass elk-rpi.yml

This will allow you to authenticate to your RPI with a password.

Troubleshoot
----------

Kibana service is not always starting. I suggest you launch it with
```
cd /opt/kibana/bin
sudo ./kibana "-c /opt/kibana/config/kibana.yml"
```

Issues are welcome.

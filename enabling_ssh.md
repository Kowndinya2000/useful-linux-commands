> Commands to setup your linux machine for remote access for others.

### Install and Enable SSH 
```
sudo apt update
sudo apt install openssh-server
```
### Start and enable the SSH service
```
sudo systemctl start ssh
sudo systemctl enable ssh
```
### Verify SSH is running:
```
systemctl status ssh
```

## Adjust firewall rules

### Allow SSH traffic through the firewall
```
sudo ufw allow ssh
# or specify port number explicitly (default is 22)
# sudo ufw allow 22/tcp
```
### Enable the firewall if it is not already active
```
sudo ufw enable
```

### Check the firewall status to confirm the rule is applied
```
sudo ufw status
```

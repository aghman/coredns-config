# coredns  
coredns configurations  

## setup guide (as root)
```shell
wget https://github.com/coredns/coredns/releases/download/v1.10.0/coredns_1.10.0_linux_amd64.tgz
tar -xvzf coredns_1.10.0_linux_amd64.tgz
sudo useradd --no-create-home --shell /usr/sbin/nologin coredns
cp coredns /usr/bin/
chown coredns:coredns /usr/bin/coredns
mkdir /etc/coredns
touch /etc/systemd/system/coredns.service
vim /etc/systemd/system/coredns.service
touch /etc/coredns/Corefile
chown -R coredns:coredns /etc/coredns
vim /etc/coredns/Corefile
touch /etc/coredns/domain.web
chown -R coredns:coredns /etc/coredns
systemctl enable coredns
systemctl start coredns 
```

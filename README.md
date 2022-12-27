# coredns  
coredns configurations  

## setup guide (as root)
```shell
wget https://github.com/coredns/coredns/releases/download/v1.10.0/coredns_1.10.0_linux_amd64.tgz
tar -xvzf coredns_1.10.0_linux_amd64.tgz
sudo useradd --no-create-home --shell /usr/sbin/nologin coredns
cp coredns /usr/bin/
mkdir /etc/coredns
vim /etc/systemd/system/coredns.service
vim /etc/coredns/Corefile
vim /etc/coredns/domain.web
chown -R coredns:coredns /etc/coredns
systemctl enable coredns
systemctl start coredns 
```

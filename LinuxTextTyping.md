## Linux Texts
 
 My recomendation use [agilefindres](https://agilefingers.com/custom-texts)

### Linux Debian Basic
```bash
ls cd pwd mkdir rmdir touch rm cp mv cat echo chmod chown df du ps top kill grep find tar zip unzip wget curl nano vi ssh scp history alias uname df ifconfig ip ping netstat ss uptime reboot shutdown passwd whoami sudo df -h ln -s man crontab service systemctl
```

### Linux Debian Networking
```bash
ping traceroute nslookup dig ifconfig ip addr ip link ip route netstat ss route iwconfig iwlist curl wget ftp scp ssh telnet nmap arp hostname whois mtr tcpdump ip neigh netcat ethtool iptraf sudo iptables -L sudo ufw status curl -I curl -X POST curl -d hostname -I finger sftp iptables-save iptables-restore
```

### Linux Debian File System Comands
```bash
ls cd pwd mkdir rmdir rm cp mv touch cat more less head tail find locate df du chmod chown ln stat file tree mount umount tar gzip gunzip zip unzip dd rsync fallocate shred chmod +x chattr lsattr quota setquota du -h df -h
```

### Linux Debian Manager Process
```bash
ps top htop pstree pgrep pidof kill killall nice renice lsof strace pmap vmstat free sar mpstat iotop watch -n 1 'ps aux' systemctl status service --status-all jobs fg bg disown nohup at crontab -l
```

### Linux Debian Firewall Iptables
```bash
sudo iptables -L  
sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT  
sudo iptables -A INPUT -p tcp --dport 443 -j ACCEPT  
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT  
sudo iptables -A INPUT -j DROP  
sudo iptables -S  
sudo iptables-save  
sudo iptables-restore  
sudo firewall-cmd --list-all  
sudo firewall-cmd --add-port=8080/tcp --permanent  
sudo firewall-cmd --reload  
sudo systemctl status firewalld  
sudo systemctl start firewalld  
sudo systemctl stop firewalld  
sudo ipset list
```

### Linux Debian Firewall ufw
```bash
sudo ufw status  
sudo ufw allow 80  
sudo ufw allow 443  
sudo ufw deny 23  
sudo ufw enable  
sudo ufw disable  
sudo ufw delete allow 80  
sudo ufw logging on  
sudo ufw reset  
sudo firewall-cmd --list-all  
sudo firewall-cmd --add-port=8080/tcp --permanent  
sudo firewall-cmd --reload  
sudo systemctl status firewalld  
sudo systemctl start firewalld  
sudo systemctl stop firewalld  
sudo ipset list
```

### Linux Debian Auditoria
```bash
tail -f /var/log/syslog
tail -f /var/log/messages
tail -f /var/log/auth.log
tail -f /var/log/secure
cat /var/log/syslog
cat /var/log/messages
cat /var/log/auth.log
cat /var/log/secure
less /var/log/syslog
less /var/log/messages
grep "erro" /var/log/syslog
grep "failed" /var/log/auth.log
grep "sudo" /var/log/auth.log
grep -i "error" /var/log/messages
awk '{print $1, $2, $3, $9}' /var/log/auth.log
journalctl -xe
journalctl -u serviço
journalctl --since "2023-10-01" --until "2023-10-18"
dmesg | less
find /var/log -type f -name "*.log" -exec grep -H "texto" {} \;
logwatch
auditctl -l
ausearch -m avc
ausearch -ts today
ausearch -ts recent
last
lastlog
who
```

### Linux APT GET
```bash
sudo apt update
sudo apt upgrade
sudo apt install package
sudo apt remove package
sudo apt purge package
sudo apt autoremove
sudo apt search termo
sudo apt show package
sudo apt list --installed
sudo apt list --upgradable
sudo apt edit-sources
sudo apt-cache policy package
sudo apt-get clean
sudo apt-get autoclean
sudo apt-mark hold package
sudo apt-mark unhold package
```

### Linux Pacman
```bash
sudo pacman -Syu
sudo pacman -S package
sudo pacman -R package
sudo pacman -Rns package
sudo pacman -Ss termo
sudo pacman -Si package
sudo pacman -Q
sudo pacman -Qe
sudo pacman -Qm
sudo pacman -Qi package
sudo pacman -Ql package
sudo pacman -Scc
sudo pacman -Fy
sudo pacman -D --asexplicit package
sudo pacman -D --asdeps package
sudo pacman -Qd
```

### Linux YUM
```bash
sudo yum update
sudo yum install package
sudo yum remove package
sudo yum search termo
sudo yum info package
sudo yum list installed
sudo yum list available
sudo yum clean all
sudo yum history
sudo yum provides arquivo
sudo yum upgrade
sudo yum groupinstall "GrupPackage"
sudo yum groupremove "GrupPackage" 
sudo yum reinstall package
sudo yum localinstall package.rpm
sudo yum --assumeyes install package
```
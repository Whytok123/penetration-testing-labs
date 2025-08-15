# Lab 2.1 – Users, Groups & Privileges

## Objective
Create a non-privileged user, grant sudo, verify access, and test editing a protected file with/without sudo.

## Commands (run as needed)
sudo adduser attacker
id attacker
sudo usermod -aG sudo attacker
getent group sudo
su - attacker
whoami
sudo -l
echo "test" > /etc/hosts    # expect: Permission denied
echo "127.0.0.1 example.local" | sudo tee -a /etc/hosts
sudo sed -i '$d' /etc/hosts  # cleanup

## Real outputs (2025-08-15 12:54:18)
```text
$ id attacker
uid=1001(attacker) gid=1001(attacker) groups=1001(attacker),27(sudo),100(users)

$ getent group sudo
sudo:x:27:kali,attacker

$ su - attacker -c whoami

$ su - attacker -c "sudo -l"

$ su - attacker -c "echo test > /etc/hosts"
Password: 
-bash: line 1: /etc/hosts: Permission denied

$ su - attacker -c "echo 127.0.0.1 example.local | sudo tee -a /etc/hosts"

$ tail -n3 /etc/hosts
ff02::1 ip6-allnodes
ff02::2 ip6-allrouters
192.168.100.138 dc0vm.youtube.local

$ sudo sed -i "$d" /etc/hosts   # cleanup last line

$ tail -n1 /etc/hosts
ff02::2 ip6-allrouters
```

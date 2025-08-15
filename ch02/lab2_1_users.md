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

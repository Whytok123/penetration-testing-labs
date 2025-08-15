# Lab 2.2 – File Permissions & Ownership

## Objective
View, change, and verify file permissions and ownership.

## Steps
echo 'secret=flag{perms}' > secret.txt
ls -l secret.txt
chmod 600 secret.txt
ls -l secret.txt
sudo chown attacker:attacker secret.txt
ls -l secret.txt
chmod u=rwx,g=rx,o= secret.txt   # 750
ls -l secret.txt

## Findings
- 600 = owner rw only; ownership change requires sudo; 750 = u:rwx g:rx o:—

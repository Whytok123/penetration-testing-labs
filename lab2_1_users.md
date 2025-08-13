# Lab 2.1 – Users, Groups & Privileges

## creat user
 bash
echo $ sudo adduser attacker
 ....(prompts) ...
echo $ id attacker
id attacketr
echo   

## Grant sudo
```bash
$ sudo usermod -aG sudo attacker
$ getent group sudo
sudo:x:27:kali,attacker
```

## Optional: Remove & restore sudo
```bash
$ sudo gpasswd -d attacker sudo
$ su - attacker && sudo -l   # expect sudoers error
$ exit
$ sudo usermod -aG sudo attacker   # restore
```

## Findings
- Created non-privileged user `attacker` and verified UID/GID.
- Granted sudo by adding to the `sudo` group; confirmed with `sudo -l`.
- Attempting to edit `/etc/hosts` without sudo failed as expected; with sudo succeeded.
- (Optional) Removing from `sudo` immediately revoked privileged actions.

## Common Errors & Fixes
- **`permission denied` when editing `/etc/*`** → use `sudo` or ensure user is in `sudo` group.
- **`user not in the sudoers file`** → `sudo usermod -aG sudo <user>`.
- **Changes not visible after group modify** → log out/in or `su - <user>` for new group membership to apply.


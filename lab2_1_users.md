# Lab 2.1 – Users, Groups & Privileges

## Objective
Create a non-privileged user, grant `sudo`, verify access, and test protected file editing with and without `sudo`.

## Environment
- Kali Linux
- Shell: zsh/bash
- Users: `kali` (admin), `attacker` (test)

## Steps & Commands
\`\`\`bash
# Create user
sudo adduser attacker
id attacker

# Grant sudo (add to sudo group)
sudo usermod -aG sudo attacker
getent group sudo

# Switch to user and verify sudo
su - attacker
whoami
sudo -l

# Negative test (no sudo) + Positive test (with sudo)
echo "test" > /etc/hosts              # expect: Permission denied
echo "127.0.0.1 example.local" | sudo tee -a /etc/hosts
tail -n3 /etc/hosts
sudo sed -i '$d' /etc/hosts           # cleanup
\`\`\`

## Example Output
\`\`\`text
(id attacker output)
(getent group sudo output)
(whoami output)
(sudo -l output)
(permission denied output)
(sudo tee output)
(tail output)
(sudo sed cleanup)
\`\`\`

## Cleanup Confirmation
\`\`\`text
192.168.100.138 dc0vm.youtube.local
✅ example.local entry removed
\`\`\`

## Findings
- Created `attacker` user and verified UID/GID.
- Granted `sudo` via `sudo` group; validated with `sudo -l`.
- Editing `/etc/hosts` failed without sudo and succeeded with sudo.
- Restored `/etc/hosts` to original state.

## Common Errors & Fixes
- **permission denied on /etc/** → use `sudo`.
- **not in the sudoers file** → `sudo usermod -aG sudo <user>` then `su - <user>` to refresh groups.
- **changes not visible** → re-run `getent group sudo` or `id <user>`.

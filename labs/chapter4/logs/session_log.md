### 2025-10-29T193322Z
- **Command**: `sudo arp-scan -l`
- **Output file**: `penetration-testing-labs/labs/chapter4/scans/2025-10-29T193322Z_sudo_arp-scan_-l.out`
- **Note**: Network ARP discovery (local network)

### 2025-10-29T193334Z
- **Command**: `sudo nmap -sn 10.10.10.0/24 -oN labs/chapter4/scans/ping_sweep.nmap`
- **Output file**: `penetration-testing-labs/labs/chapter4/scans/2025-10-29T193334Z_sudo_nmap_-sn_10.10.10.0_24_-oN_labs_chapter4_scans_ping_swe.out`
- **Note**: Ping sweep subnet 10.10.10.0/24

### 2025-10-29T193421Z
- **Command**: `sudo nmap -sS -sV -T4 --open -oN labs/chapter4/scans/quick_svc_10.10.10.5.nmap 10.10.10.5`
- **Output file**: `penetration-testing-labs/labs/chapter4/scans/2025-10-29T193421Z_sudo_nmap_-sS_-sV_-T4_--open_-oN_labs_chapter4_scans_quick_s.out`
- **Note**: Fast service discovery on host 10.10.10.5

### 2025-10-29T193433Z
- **Command**: `sudo nmap -p- -sC -sV -T4 -oN labs/chapter4/scans/full_svc_10.10.10.5.nmap 10.10.10.5`
- **Output file**: `penetration-testing-labs/labs/chapter4/scans/2025-10-29T193433Z_sudo_nmap_-p-_-sC_-sV_-T4_-oN_labs_chapter4_scans_full_svc_1.out`
- **Note**: Full TCP port scan & NSE scripts


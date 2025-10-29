# Chapter 4 Report


#### 2025-10-29T193322Z
**Command:** `sudo arp-scan -l`  
**Note:** Network ARP discovery (local network)  
**Output:** `penetration-testing-labs/labs/chapter4/scans/2025-10-29T193322Z_sudo_arp-scan_-l.out`


#### 2025-10-29T193334Z
**Command:** `sudo nmap -sn 10.10.10.0/24 -oN labs/chapter4/scans/ping_sweep.nmap`  
**Note:** Ping sweep subnet 10.10.10.0/24  
**Output:** `penetration-testing-labs/labs/chapter4/scans/2025-10-29T193334Z_sudo_nmap_-sn_10.10.10.0_24_-oN_labs_chapter4_scans_ping_swe.out`


#### 2025-10-29T193421Z
**Command:** `sudo nmap -sS -sV -T4 --open -oN labs/chapter4/scans/quick_svc_10.10.10.5.nmap 10.10.10.5`  
**Note:** Fast service discovery on host 10.10.10.5  
**Output:** `penetration-testing-labs/labs/chapter4/scans/2025-10-29T193421Z_sudo_nmap_-sS_-sV_-T4_--open_-oN_labs_chapter4_scans_quick_s.out`


#### 2025-10-29T193433Z
**Command:** `sudo nmap -p- -sC -sV -T4 -oN labs/chapter4/scans/full_svc_10.10.10.5.nmap 10.10.10.5`  
**Note:** Full TCP port scan & NSE scripts  
**Output:** `penetration-testing-labs/labs/chapter4/scans/2025-10-29T193433Z_sudo_nmap_-p-_-sC_-sV_-T4_-oN_labs_chapter4_scans_full_svc_1.out`


#### 2025-10-29T193448Z
**Command:** `gobuster dir -u http://10.10.10.5 -w /usr/share/seclists/Discovery/Web-Content/common.txt -o labs/chapter4/scans/gobuster_10.10.10.5.txt -t 40`  
**Note:** Gobuster directory enumeration  
**Output:** `penetration-testing-labs/labs/chapter4/scans/2025-10-29T193448Z_gobuster_dir_-u_http__10.10.10.5_-w__usr_share_seclists_Disc.out`


#### 2025-10-29T193833Z
**Command:** `nikto -h http://10.10.10.5 -output labs/chapter4/scans/nikto_10.10.10.5.txt`  
**Note:** Nikto web vuln scan (non-destructive)  
**Output:** `penetration-testing-labs/labs/chapter4/scans/2025-10-29T193833Z_nikto_-h_http__10.10.10.5_-output_labs_chapter4_scans_nikto_.out`


#### 2025-10-29T193930Z
**Command:** `sqlmap -u "http://10.10.10.5/page.php?id=1" --batch --level=1 --risk=1 --forms --crawl=1 --dbs --answers="quit=Y" `  
**Note:** sqlmap detection (non-destructive) on probable param  
**Output:** `penetration-testing-labs/labs/chapter4/scans/2025-10-29T193930Z_sqlmap_-u_http__10.10.10.5_page.phpid1_--batch_--level1_--ri.out`


#### 2025-10-29T194119Z
**Command:** `curl -s "http://10.10.10.5/search?q=<script>alert(1)</script>" | grep -i "<script>alert(1)</script>" || echo 'Not reflected'`  
**Note:** Quick XSS reflection test  
**Output:** `penetration-testing-labs/labs/chapter4/scans/2025-10-29T194119Z_curl_-s_http__10.10.10.5_searchqscriptalert1_script__grep_-i.out`


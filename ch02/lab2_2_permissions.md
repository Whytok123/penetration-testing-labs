# Lab 2.2 – File Permissions & Ownership

_Started: Fri Aug 15 03:01:46 PM EDT 2025_

```bash
$ echo 'secret=flag{perms}' > ch02/secret.txt
```
```

```
_Exit code: 
```bash
$ ls -l ch02/secret.txt
```
```
-rw-rw-r-- 1 kali kali 19 Aug 15 15:01 ch02/secret.txt
```
_Exit code: 
```bash
$ chmod 600 ch02/secret.txt
```
```

```
_Exit code: 
```bash
$ ls -l ch02/secret.txt
```
```
-rw------- 1 kali kali 19 Aug 15 15:01 ch02/secret.txt
```
_Exit code: 
```bash
$ sudo chown attacker:attacker ch02/secret.txt
```
```

```
_Exit code: 
```bash
$ ls -l ch02/secret.txt
```
```
-rw------- 1 attacker attacker 19 Aug 15 15:01 ch02/secret.txt
```
_Exit code: 
```bash
$ chmod u=rwx,g=rx,o= ch02/secret.txt
```
```
chmod: changing permissions of 'ch02/secret.txt': Operation not permitted
```
_Exit code: 
```bash
$ ls -l ch02/secret.txt
```
```
-rw------- 1 attacker attacker 19 Aug 15 15:01 ch02/secret.txt
```
_Exit code: 
💡 600 = owner-only read/write; 750 = owner: rwx, group: rx, others: none. chown changes ownership to attacker.

**Lab 2.2 complete – file permissions & ownership outputs saved**
_Ended: Fri Aug 15 03:01:50 PM EDT 2025_
```bash
$ chmod u=rwx,g=rx,o= ch02/secret.txt
```
```
chmod: changing permissions of 'ch02/secret.txt': Operation not permitted
```
_Exit code: 
```bash
$ ls -l ch02/secret.txt
```
```
-rw------- 1 attacker attacker 19 Aug 15 15:01 ch02/secret.txt
```
_Exit code: 

**Lab 2.2 – Fixed chmod output**
_Ended: Fri Aug 15 03:04:53 PM EDT 2025_

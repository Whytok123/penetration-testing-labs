# lab 3.1 - filesystem navigation

_Started: Tue Aug 19 03:55:25 PM EDT 2025_

```bash
$ pwd
```
```
/home/kali/penetration-testing-labs
```
_Exit code: 
```bash
$ ls -la
```
```
total 36
drwxrwxr-x  7 kali kali 4096 Aug 19 15:55 .
drwx------ 18 kali kali 4096 Aug 19 15:53 ..
drwxrwxr-x  2 kali kali 4096 Aug 15 14:51 $(dirname $r)
-rw-rw-r--  1 kali kali   88 Aug 15 14:57 $LAB_REPORT
drwxrwxr-x  2 kali kali 4096 Aug 15 11:48 ch01
drwxrwxr-x  2 kali kali 4096 Aug 15 15:26 ch02
drwxrwxr-x  2 kali kali 4096 Aug 19 15:55 ch03
drwxrwxr-x  8 kali kali 4096 Aug 15 15:04 .git
-rw-rw-r--  1 kali kali  217 Aug 15 11:55 README.md
```
_Exit code: 
```bash
$ cd /etc && pwd
```
```
/etc
```
_Exit code: 
```bash
$ ls -l passwd
```
```
ls: cannot access 'passwd': No such file or directory
```
_Exit code: 
```bash
$ cd ~ && pwd
```
```
/home/kali
```
_Exit code: 
💡 Practiced navigating with cd, pwd, ls; learned relative vs absolute paths.

**Lab 3.1 complete – filesystem navigation**
_Ended: Tue Aug 19 03:56:37 PM EDT 2025_
💡 Practiced navigating with cd, pwd, ls; learned relative vs absolute paths.

**Lab 3.1 complete – filesystem navigation**
_Ended: Tue Aug 19 03:59:53 PM EDT 2025_

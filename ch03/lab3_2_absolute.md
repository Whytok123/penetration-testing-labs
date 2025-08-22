# Lab 3.2 – Absolute Paths

_Started: Fri Aug 22 02:09:14 PM EDT 2025_

```bash
$ mkdir -p ~/penetration-testing-labs/ch03/lab2
```
```

```
_Exit code: 
```bash
$ echo 'Absolute path test' > ~/penetration-testing-labs/ch03/lab2/abs.txt
```
```

```
_Exit code: 
```bash
$ cat /home/kali/penetration-testing-labs/ch03/lab2/abs.txt
```
```
Absolute path test
```
_Exit code: 
```bash
$ cd /tmp && cat /home/kali/penetration-testing-labs/ch03/lab2/abs.txt
```
```
Absolute path test
```
_Exit code: 
```bash
$ pwd
```
```
/home/kali/penetration-testing-labs
```
_Exit code: 
```bash
$ cat /home/kali/penetration-testing-labs/ch03/lab2/abs.txt
```
```
Absolute path test
```
_Exit code: 
💡 Absolute paths always begin with / and work from any directory. Unlike relative paths, they are independent of current working location.

**Lab 3.2 complete – absolute paths outputs saved**
_Ended: Fri Aug 22 02:09:14 PM EDT 2025_

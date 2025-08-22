# Lab 3.5 – mkdir, rmdir, and rm

_Started: Fri Aug 22 05:22:11 PM EDT 2025_

```bash
$ mkdir -p ch03/lab3_5_demo
```
```

```
_Exit code: 
```bash
$ echo 'test file inside lab3_5' > ch03/lab3_5_demo/note.txt
```
```

```
_Exit code: 
```bash
$ ls -l ch03/lab3_5_demo
```
```
total 4
-rw-rw-r-- 1 kali kali 24 Aug 22 17:22 note.txt
```
_Exit code: 
```bash
$ rmdir ch03/lab3_5_demo
```
```
rmdir: failed to remove 'ch03/lab3_5_demo': Directory not empty
```
_Exit code: 
```bash
$ rm -r ch03/lab3_5_demo
```
```

```
_Exit code: 
```bash
$ ls -l ch03
```
```
total 32
drwxrwxr-x 2 kali kali 4096 Aug 22 14:06 lab2
-rw-rw-r-- 1 kali kali 1197 Aug 19 15:59 lab3_1_navigation.md
-rw-rw-r-- 1 kali kali  925 Aug 22 14:09 lab3_2_absolute.md
drwxrwxr-x 3 kali kali 4096 Aug 22 14:15 lab3_3
-rw-rw-r-- 1 kali kali  350 Aug 22 14:41 lab3_3_paths.md
-rw-rw-r-- 1 kali kali  591 Aug 22 16:53 lab3_4_cd.md
-rw-rw-r-- 1 kali kali  557 Aug 22 17:22 lab3_5_dirs.md
drwxrwxr-x 2 kali kali 4096 Aug 19 16:00 screenshots
```
_Exit code: 
💡 mkdir creates directories, rmdir removes empty ones, rm -r removes directories even if not empty. rm -rf is dangerous because it forces deletion recursively.

**Lab 3.5 complete – mkdir, rmdir, and rm**
_Ended: Fri Aug 22 05:22:11 PM EDT 2025_

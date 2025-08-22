# Lab 3.6 – Copy & Move

_Started: Fri Aug 22 06:07:22 PM EDT 2025_

```bash
$ echo 'important notes' > ch03/notes.txt
```
```

```
_Exit code: 
```bash
$ cp ch03/notes.txt ch03/notes_copy.txt
```
```

```
_Exit code: 
```bash
$ ls -l ch03/
```
```
total 48
drwxrwxr-x 2 kali kali 4096 Aug 22 14:06 lab2
-rw-rw-r-- 1 kali kali 1197 Aug 19 15:59 lab3_1_navigation.md
-rw-rw-r-- 1 kali kali  925 Aug 22 14:09 lab3_2_absolute.md
drwxrwxr-x 3 kali kali 4096 Aug 22 14:15 lab3_3
-rw-rw-r-- 1 kali kali  350 Aug 22 14:41 lab3_3_paths.md
-rw-rw-r-- 1 kali kali  591 Aug 22 16:53 lab3_4_cd.md
-rw-rw-r-- 1 kali kali 1274 Aug 22 17:22 lab3_5_dirs.md
-rw-rw-r-- 1 kali kali  247 Aug 22 18:07 lab3_6_cp_mv.md
drwxrwxr-x 2 kali kali 4096 Aug 22 18:02 lab3_6_demo
-rw-rw-r-- 1 kali kali   16 Aug 22 18:07 notes_copy.txt
-rw-rw-r-- 1 kali kali   16 Aug 22 18:07 notes.txt
drwxrwxr-x 2 kali kali 4096 Aug 19 16:00 screenshots
```
_Exit code: 
```bash
$ mv ch03/notes_copy.txt ch03/notes_archive.txt
```
```

```
_Exit code: 
```bash
$ ls -l ch03/
```
```
total 48
drwxrwxr-x 2 kali kali 4096 Aug 22 14:06 lab2
-rw-rw-r-- 1 kali kali 1197 Aug 19 15:59 lab3_1_navigation.md
-rw-rw-r-- 1 kali kali  925 Aug 22 14:09 lab3_2_absolute.md
drwxrwxr-x 3 kali kali 4096 Aug 22 14:15 lab3_3
-rw-rw-r-- 1 kali kali  350 Aug 22 14:41 lab3_3_paths.md
-rw-rw-r-- 1 kali kali  591 Aug 22 16:53 lab3_4_cd.md
-rw-rw-r-- 1 kali kali 1274 Aug 22 17:22 lab3_5_dirs.md
-rw-rw-r-- 1 kali kali 1038 Aug 22 18:07 lab3_6_cp_mv.md
drwxrwxr-x 2 kali kali 4096 Aug 22 18:02 lab3_6_demo
-rw-rw-r-- 1 kali kali   16 Aug 22 18:07 notes_archive.txt
-rw-rw-r-- 1 kali kali   16 Aug 22 18:07 notes.txt
drwxrwxr-x 2 kali kali 4096 Aug 19 16:00 screenshots
```
_Exit code: 
```bash
$ mkdir -p ch03/lab3_6_demo
```
```

```
_Exit code: 
```bash
$ mv ch03/notes_archive.txt ch03/lab3_6_demo/
```
```

```
_Exit code: 
```bash
$ ls -l ch03/lab3_6_demo/
```
```
total 4
-rw-rw-r-- 1 kali kali 16 Aug 22 18:07 notes_archive.txt
```
_Exit code: 
💡 We practiced cp (copy), mv (rename), and mv into folder. Notes file was copied, renamed, and then moved into lab3_6_demo/.

**Lab 3.6 complete – Copy & Move commands practiced**
_Ended: Fri Aug 22 06:07:22 PM EDT 2025_

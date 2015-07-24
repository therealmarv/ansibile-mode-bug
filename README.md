# Bug in Ansible 1.9.2

Shows a file copy error when using YAML mode in a different format.

Clone this repo and run:
```
vagrant up
```

go to temp and see the results:
```
vagrant ssh
cd /tmp
ls -all
```

Result you will see with **bug** in first dummy file:
```
vagrant@vagrant-ubuntu-trusty-32:~$ cd /tmp
vagrant@vagrant-ubuntu-trusty-32:/tmp$ ls -all
total 48
drwxrwxrwt  4 root root 4096 Jul 24 18:29 .
drwxr-xr-x 22 root root 4096 Jul 24 18:29 ..
--wxrw--wt  1 root root    4 Jul 24 18:29 dummy1
-rwxr-xr-x  1 root root    4 Jul 24 18:29 dummy2
-rwxr-xr-x  1 root root    4 Jul 24 18:29 dummy3
-rwxr-xr-x  1 root root    4 Jul 24 18:29 dummy4
-rwxr-xr-x  1 root root    4 Jul 24 18:29 dummy5
-rwxr-xr-x  1 root root    4 Jul 24 18:29 dummy6
-rwxr-xr-x  1 root root    4 Jul 24 18:29 dummy7
-rwxr-xr-x  1 root root    4 Jul 24 18:29 dummy8
```

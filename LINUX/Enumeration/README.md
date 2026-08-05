There are five stages of hacking. First 3 stages are Information Gathering, Scanning and enumeration, and exploitation

# Enumeration

## System Enumeration

```bash
# What is the kernel is. After the check of google if there is any exploitation is
$ uname -a
$ cat /proc/version
$ cat /etc/issue
$ lscpu

# Check What services are Running
$ ps -aux

# Pool out all the root users
$ ps -aux | grep root

# Note : It always important to know What Host Name the server is
```

## User Enumeration

```bash
# Who is the User
$ whoami

# What are the Id of that User
$ id

# What privileges we might have
$ sudo -l

# We can check the password of a user
$ cat /etc/passwd
$ cat /etc/shadow

# Pool out all the user
$ cat /etc/passwd | cut -d : -f 1
```

## Network Enumeration

```bash

# Check Network
$ ifconfig
$ ip a
$ ip a s

# Command of Route
$ route
$ ip route

# Traffic to the internet that has been generated through out the pc
$ arp -a
$ ip neigh

# all
$ netstat -alo
```

## Password Enumeration

```bash

```

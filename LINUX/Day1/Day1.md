## Terminal, TTY and Bash

- _Terminal (The Visual Wrapper)_
  - A Terminal is a graphical application that provides a user interface. It has no understanding of commands like ls or cd.
- _TTY (The OS Link)_
  - TTY stands for TeleTypeWriter. In modern OS a TTY is a abstract software device insides the IS kernel. It acts a middleman that handle the flow of text data between your Terminal application and the shell. Like An HTTP Request.
- _Bash(The Brain)_
  - Bourne-Again Shell is the actual command-line interpreter software. it is a user space application that sits waiting for text input. When you type a command and hit enter Bash parses the string, determines what you to achieve with the OS kernel to execute it, and the passes the result back.

## Basic Command Line Interface

- _Username_
  - whoami
  - id
- _hostname_
  - hostname
- _working directory_
  - pwd
- _Environment Variable_
  - env
- _Which (and $PATH)_
  - which pwd
  - It will tell which file is for that particular program

## Absolute Path and Relative Path

- _Absolute Path_
  - It always start with root (/) of the file system
  - /home/badhon/option
- _Relative Path_
  - Relative path Is start with Current Working Directory
  - ../../carts-oscp/full

## File System Commands

Command to move in the _File System_

- _Working Directory_
  - pwd
- _Change Directory_
  - cd
  - cd ..
  - cd Folder/Directory
- _List Files_
  - ls
  - ls -alth
  - ls -alh
- _echo_
  - echo "Hello1" > text.txt # The Output of the echo will print here
  - cat text.txt # Cat is the program and tet.txt is the argument
  - cat text1.txt text2.txt
- _Move Files_
  - mv
  - mv hello.txt hello2.txt
  - mv hello.txt /tmp/
- _Copy Files_
  - cp hello.txt hello2.txt
- _Remove Files_
  - rm hello
  - rm - rf hello

## Resources Management

- _Disk Devices_
  - fdisk -l
- _Disk usage_
  - df -h
  - du -h
- _Processes_ : Processes bounds by controlling terminal
  - ps
- _View system processes_
  - ps aux
- _show hierarchy_
  - ps -axjf
- _Network interfaces_
  - ip address
  - ip a
  - ip a s
- _Open Ports_ : display all TCP listening ports, displaying pid/program names and resolve names with IP address
  - netstat -ltp

## Users Managements Commands

- Create new user with default settings
  - sudo useradd -m <USERNAME>
- Changed User Password
  - sudo passwd <USERNAME>
- Delete User
  - sudo userdel -r <USERNAME>
- List groups of a given user
  - groups <USERNAME>
- Create new group
  - groupadd <GROUPNAME>
- Add user to group
  - usermod -a -G <GroupName> <UserName>
- Tow Foundamental files related to user management are
  - ~/etc/password : Contains useful metadata for users.

## Package Managements

- In order to manage system packages we can use ~apt~ or ~ apt-get~.
- Install
  - apt-get install fdisk
- Search
  - apt search disk
- Remove
  - apt-get purge fdisk
- Update

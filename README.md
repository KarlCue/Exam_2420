# Exam_2420

# Part 1
sudo apt update | sudo apt upgrade

# Part 2
##:%s/numbs/:digits:
##:%s/eco/echo
##:%s/V/C

then press a for all occurances

# Part 4
```
#!/bin/bash
#: Title       : Finding Users
#: Date        : December 8 2022
#: Author      : Karl Cue
#: Project     : Finals
#: Description : Print System Information
#: Options     : None

echo -e "Regular users on the system are:
$(cat /etc/passwd | grep -E 100[0-5] /etc/passwd | awk -F: '{print $1 ,$3 ,$7}')"
echo -e " "
echo -e "Users currently logged in are:
$(who | awk '{print $1}')"
```
# Part 5
written in bin/finals
```
[Unit]
Description=Look for regular users and active users

[Service]
type=oneshot
ExecStart=/bin/finals/find_users

[Install]
WantedBy=multi-user.target
```

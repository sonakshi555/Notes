she bang
#!/bin/bash

Add meta data like author ,date , description and version of the script

**set -x** :  DEBUG mode .
displays the output of the commands like 
+nproc
1
to know the command instead of echo the command which we are using

**set -e** :  exits the script and stop running it ,when it find out error.
if this is not used , the whole scripts is executed and won't able to find the error line in 100+ output lines

**set -o** : pipe fail 
it is used to avoid the failure in case of "set -e" ignores it
This happens because usually set -e is ignores when there is any error in pipped output
example : sjfbajsdbfdsbff | echo 
Here set -e ignores the error as it cares about the last command 
since "echo" is valid command so it is executed without exiting it
So set -o is used to avoid this issue

>> awk
 curl
 wget
 find:
 example : sudo find / -name file_name
 sudo : substitute user do or super user do
 su : switch user
    if [ expression ]
    then
    else
for i in {1.100}; do 
trap : it is a command used to trap signals and it is tricky
trap the commands and performs execution on my behalf like interrupting them and execute what i want it do

sar 

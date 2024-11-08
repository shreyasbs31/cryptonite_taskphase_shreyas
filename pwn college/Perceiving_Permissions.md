# Perceiving Permissions

## Changing File Ownership
i did chown hacker /flag to change the ownership of the /flag file and then used cat to get the flag
```
pwn.college{QvVWpg9P3zJAtGv7fKrzzZQnBq5.dFTM2QDLzkDO0czW}
```
##

## Groups and Files
i first did chgrp hacker /flag to change the group and then cat /flag to get the flag
```
pwn.college{oJfLPTIbKKvqW5Ezd6R9DyhvHEt.dFzNyUDLzkDO0czW}
```
##

## Fun With Groups Names
change group of /flag to user's group
```
pwn.college{MSi7s-erW4whyFKzYfW2_uQcQf9.dJzNyUDLzkDO0czW}
```
##

## Changing Permissions
i did chmod u+r to add read to the user and then did cat to read the /flag file
```
pwn.college{EcB9YWaU_GId-t_ErIDDyty9iwM.dNzNyUDLzkDO0czW}
```
##

## Executable Files
i did chmod u+x /challenge/run to allow me to execute the /challenge/run file and then i ran it to get my flag
```
pwn.college{EXtIDBOg6eIkomc2hf4zzJ6Ni7C.dJTM2QDLzkDO0czW}
```
##

## Permission Tweaking Practice
i did exactly what was asked in the challenge and ran through chmod practice basically
```
pwn.college{IrMBX8AOY0qF1KZz2K_qVsTUL_Z.dBTM2QDLzkDO0czW}
```
## Permissions Setting Practice
i learnt how to set permissions also using chmod and = sign
```
pwn.college{41pPV8PyIsle2eG9tWMG7XkBGkv.dNTM5QDLzkDO0czW}
```
## 

## The SUID Bit
chmod u+s /challenge/getroot and then cat /flag to get root/
```
pwn.college{QhVTfGtpWV2dSmm-K3BMcO2Ezn_.dNTM2QDLzkDO0czW}
```
##

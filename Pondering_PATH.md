# Pondering PATH

## The PATH Variable
i removed the value of PATH so that it could never access /challenge/run so i did PATH="" and then /challenge/run
```
pwn.college{cGm0GRj3_vUZxgYREYfwaqvUbMX.dZzNwUDLzkDO0czW}
```
##

## Setting PATH
i set PATH=/challenge/more_commands/ and then ran /challenge/run to get my flag
```
pwn.college{MQMvN6bV-G8bFjtTXfmIMOTGUvs.dVzNyUDLzkDO0czW}
```
##

## Adding Commands
After a lot of researching and searching around and discussions, i first created a file win using touch win. then i did echo "cat /flag" > win to store it in win, then made win executable by chmod ugo+x win. Then i analysed PATH using echo $PATH and set PATH=$PATH:/home/hacker. then i ran /challenge/run to get my flag
```
pwn.college{4_FYhp36_lVLSjTP7wYbeRYJ4bS.dZzNyUDLzkDO0czW}
```
##

## Hijacking Commands
After a ton of headscratching and figuring out what to do and talking to many many people about it, i finally understood what needs to be done. I did echo cat /flag > rm, and then set PATH=~:$PATH, and then made the rm command executable by chmod a+x rm, and then finally ran /challenge/run.
The reason i did this is because, i know the shell checks the PATH from left to right for the command to execute, so i had to ensure i created a duplicate rm(which i set to read the flag instead of delete) which ran before the actual rm hence i did PATH=~:$PATH, so that the duplicate rm will be invoked before the actual rm and the file will be read successfully on running /challenge/run.
```
pwn.college{Aiy-QMuRNHs8r7g307V9AO5DYd1.ddzNyUDLzkDO0czW}
```
##
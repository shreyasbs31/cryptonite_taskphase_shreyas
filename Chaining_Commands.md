# Chaining Commands

## Chaining with Semicolons
i understood what ; does, and so i ran /challenge/pwn; /challenge/college to get my flag.
```
pwn.college{0BUGLqYfphAnL2hOLgLoV3H649k.dVTN4QDLzkDO0czW}
```
##

## Your First Shell Script
i didn't understand what to do, and i was lost for a very long time, so i researched a little here and there and found a command called nano, so i created a x.sh file using touch command and then did nano x.sh to edit the shell script and then added /challenge/pwn; /challenge/college in it. Finally i did bash x.sh to get my flag
```
pwn.college{0krhgdSG9i-8InG50KXtlM69faq.dFzN4QDLzkDO0czW}
```
## 

## Redirecting Script Output
i had to pipe the output from x.sh into /challenge/solve, so i did bash x.sh | /challenge/solve
```
pwn.college{csaIux3d4fHduf6tA62_KxRpM6j.dhTM5QDLzkDO0czW}
```
##

## Executable Shell Scripts
i created a shell script called script.sh and then used nano to edit the shell script and added /challenge/solve in it and then changed its permissions using chmod u+x script.sh and then ran it using ./script.sh
```
pwn.college{Az88CJJJwFAGdcBOEFbOBUXoTAw.dRzNyUDLzkDO0czW}
```
##
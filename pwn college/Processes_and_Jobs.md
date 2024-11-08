# Processes and Jobs

## Listing Processes
i first did ps -ef to list out all the processes, and then i used /challenge/26026-run-4063
```
pwn.college{YNHgQEhTUMzQsG09OJEiDiwAp6U.dhzM4QDLzkDO0czW}
```
##

## Killing Processes
i understood what the kill command is.
first i did ps -ef and found the PID of /challenge/dont_run and then did kill 73(the PID) to kill the process and then ran /challenge/run to get the key
```
pwn.college{sNGq6Ra-y2l6Pao6m4r68qUv0sN.dJDN4QDLzkDO0czW}
```
##

## Interrupting Processes
i did /challenge/run and then Ctrl+C to interrupt it to get my flag
```
pwn.college{4TO_CZTq1kCFMXgIVjn15ZGzc3h.dNDN4QDLzkDO0czW}
```
##

## Suspending Processes
i ran /challenge/run and then suspended it using Ctrl+Z and then again ran /challenge/run to get my flag
```
pwn.college{gxDS475frQ84ON5WjMfEwTqV7bI.dVDN4QDLzkDO0czW}
```
##

## Resuming Processes
like before, i suspended /challenge/run and then resumed it using fg 
```
pwn.college{AZ0UcIlCAUszYdfxNlJH6UrnNDE.dZDN4QDLzkDO0czW}
```
##

## Backgrounding Processes
i first did /challenge/run and then suspended it and resumed it again in the background using bg and then ran another /challenge/run to get my flag as asked in the question.
```
pwn.college{0hSlHpllT1K0QBsZlScPW2pG2Wc.ddDN4QDLzkDO0czW}
```
##

## Foregrounding Processes
it was literally the same as previous ones, i just used fg to make the background task come back to the foreground.
```
pwn.college{Qz5FdXPidQ1TYFAwlbEpJ_EfcAd.dhDN4QDLzkDO0czW}
```
##

## Starting Backgrounded Processes
i did /challenge/run & 
```
pwn.college{UCnALAIzThxoZNoljgGrg-u8Xvg.dlDN4QDLzkDO0czW}
```
##

## Process Exit Codes
i first did /challenge/get-code and then immediately did echo $? to get the error code '230' and then ran /challenge/submit-code 230 to get the flag
```
pwn.college{wUlTdPhYpDnUpJ9wOodgzANlmML.dljN4UDLzkDO0czW}
```
##

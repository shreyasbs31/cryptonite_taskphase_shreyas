# Practicing Piping 

## Challenge 1: Redirecting output
i used the echo command and then redirected the output to COLLEGE
```
pwn.college{cOTI8WdZD9KOmegn_FTEjE4yxU5.dRjN1QDLzkDO0czW}
```
##

## Challenge 2: Redirecting more output
i redirected the output of /challenge/flag to myflag and then used the cat command.
```
pwn.college{IlhkyKm_IpT3cIYeFklfLLrNgc9.dVjN1QDLzkDO0czW}
```
##

## Challenge 3: Appending output
i redirected the output of /challenge/run to /home/hacker/the-flag and then appended /challenge/run again using >> to /home/hacker/the-flag and then used the cat command. 
```
pwn.college{8vywi5HXq_1XFBLxi8XJt9qwMBT.ddDM5QDLzkDO0czW}
```
##

## Challenge 4: Redirecting errors
i redirected everything as asked in question
```
pwn.college{gpGWR8YqtNdBpc34K9t-8qZBdIw.ddjN1QDLzkDO0czW}
```
## 

## Challenge 5: Redirecting input
i created a pwn file which contained the word college, and then redirected its input into /challenge/run 
```
pwn.college{IpwRMUCAgHlVLqMkt-C-U3XnQ0p.dBzN1QDLzkDO0czW}
```
##

## Challenge 6: Grepping stored results
first i redirected the output as asked, and then used grep to search for pwn and found the flag.
```
pwn.college{8Edjjrk-mvISjyxgulttIO8dqeI.dhTM4QDLzkDO0czW}
```
##

## Challenge 7: Grepping live output
i did what was asked in the question
```
pwn.college{wZsOgzhyrZXE5FiTw920CkZ_vOI.dlTM4QDLzkDO0czW}
```
##

## Challenge 8: Grepping errors
i understood what the >& operator is and got the flag by following what was asked
```
pwn.college{M3qKoZDINIYDoD06K98cqfcUnFP.dVDM5QDLzkDO0czW}
```
## 

## Challenge 9: Duplicating piped data from tee
i won't lie, i didn't actually understand what this challenge was. All i know is the | command doesn't store the output anywhere but it will do so if passed with tee. For this challenge i had to run /challenge/pwn | tee a | /challenge/college and then read a for the code and then run /challenge/pwn --secret UjM9G0d_ | /challenge/college for the flag
```
pwn.college{ckzLZajbKWkK0uc1Ydr74Ni49Ue.dFjM5QDLzkDO0czW}
```
##

## Challenge 10: Writing to multiple programs
if you write an argument of >(rev), bash will run the rev command but put its input to a temporary file that it will create. so i had to take output of /challenge/hack and pass it as input to the files /challenge/the and /challenge/planet files
```
pwn.college{Yiq_FOdKWiBmpnTPO17UcYsnr6w.dBDO0UDLzkDO0czW}
```
##

## Challenge 11: Split-piping sterr and stdout
i won't lie, i didn't completely understand this one either, but basically what i think i did was i connected the output of /challenge/hack to /challenge/input and all the errors of /challenge/hack to /challenge/the by using the >> command and then using 2>> to redirect all the errors.
```
pwn.college{MRmOgu6PgMN_sclE9PUlRlOcOAq.dFDNwYDLzkDO0czW}
```
##



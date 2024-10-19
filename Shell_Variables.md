# Shell Variables

## Printout Variables
i used the command echo $FLAG
'''
pwn.college{ktBOV3naec842xyb5EUgVuokC_S.ddTN1QDLzkDO0czW}
'''
##

## Setting Variables
i just did PWN=COLLEGE and got the flag?
'''
pwn.college{ciGfMhId7e5ZliY7DjIvcq2fQCv.dlTN1QDLzkDO0czW}
'''
##

## Multi-word Variables
PWN="COLLEGE YEAH" (basically how strings also work)
'''
pwn.college{gOS0T55NAXhdb3JwPQL_u03HYPC.dBjN1QDLzkDO0czW}
'''
##

## Exporting Variables
i first did PWN=COLLEGE and then exported PWN, and then did COLLEGE=PWN and then ran /challenge/run to get the flag
```
pwn.college{03Me-eakFPFj0FZ2ZD9o3jdAZ7d.dJjN1QDLzkDO0czW}
```
##

## Printing Exported Variables
i did env and then found the flag variable
```
pwn.college{w8PGyawtFXx4FQwmD3sDZEUU0iu.dhTN1QDLzkDO0czW}
```
##

## Storing Command Output
i did PWN=$(/challenge/run), and then echo $PWN
```
pwn.college{skYJJOenbUyYupIfwwRtINLHyDy.dVzN0UDLzkDO0czW}
```
##

## Reading Input
i understood what the read command does, and then did read PWN and set that value to COLLEGE to get my flag
```
pwn.college{Y6rZ9uNO_A9r0QNr409JIar57uw.dhzN1QDLzkDO0czW}
```
##

## Reading Files
i did read PWN < /challenge/read_me to read the /challenge/read_me directly into PWN.
```
pwn.college{I076tqYnVHf4W8GHJ7MTPN7u7zA.dBjM4QDLzkDO0czW}
```
##
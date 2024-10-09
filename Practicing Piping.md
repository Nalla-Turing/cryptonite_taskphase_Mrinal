# Practicing Piping
This module is about teaching he basics of 3 main channels in a linux communication channel

`stdin` That handles input
`stdout` That handles output
`stderr` That handles errors
<br><br><br>

## Challenge - 1 Redirecting Output
You can redirect your output a file and then later cat that file to learnw hat is the output

For the challenge i `eho PWN > COLLEGE ` to add PWN text to COLLEGE file

flag `pwn.college{ceMMRkoUHqn2NTTadpEmR67iHM0.dRjN1QDL0MTO0czW}`
<br><br>

## Challenge - 2 Redirecting more output
It's not just `echo` whose output we can redirect. We can also redirect the output of any command.

In this challenge, i redirect the output of `/challenge/run > myflag` and then `cat myflag` to get the flag

flag `pwn.college{4bUMlsqeWyflsHrbgtVoImtUt6w.dVjN1QDL0MTO0czW}`
<br><br>

## Challenge - 3 Appending Ouput 
We came to know that if you add the output of multiple comands to a file using `>` each time, the output will overwrite the output pof previous one.

So to get around that we use `>>` or Append pipe

For the challenge `/challenge/run >> /home/hacker/the-flag`
This will append the first half of the file and on completion the shell will add the second half of the file to it's stdout channel.

flag `pwn.college{kS_qnuqnP-yv1iPRz0fGLRkIObr.ddDM5QDL0MTO0czW}`
<br><br>

## Challenge - 4 Redirecting errors

<br><br>

## Challenge - 5 Redisrecting input
<br><br>

## Challenge - 6 Grepping stored results
<br><br>

## Challenge - 7 Grepping live output
<br><br>

## Challenge - 8 Grepping errors
<br><br>

## Challenge - 9 Duplicating piped data with tee
<br><br>

## Challenge - 10 Writing to multiple programs 
<br><br>

## Challenge - 11 Split-piping stderr and stdout
<br><br>
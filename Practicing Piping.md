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
Hre we learn that we can output multiple aspects in the same line. We jsut need specify the file descriptor number before the pipe `>`
1 is for standard output and 2 is for errors usually 

For the challenge `/challenge/run > myflag 2> instructions` is to output flag to myflag and instructions to instructions 
`cat instructions`
and `cat myflag` to get the flag
flag `pwn.college{0zmbZ7tW3hEimeZZtCOqUC8kxKG.ddjN1QDL0MTO0czW}`
<br><br>

## Challenge - 5 Redisrecting input
You can redirect input to a file using `<` command.

For the challenge redirect output COLLEGE to PWN
` echo COLLEGE > PWN`

Now redirect the input of PWN  file to /chalenge/run command using
`/challenge/run < PWN` to get the flag

flag `pwn.college{wm6U8M9ARmVbIiyUK471Xy7E77A.dBzN1QDL0MTO0czW}`
<br><br>

## Challenge - 6 Grepping stored results
This challenge is about using grepping along with our pipe commands.

For the challenge I move the output of `/challenge/run > /tmp/data.txt`
Then to get the flag form our output file,
search pwn from the file using `grep pwn /tmp/data.txt` giving us the flag.

flag `pwn.college{wcxwc0WZ-55jfYQwXEW5dNQyweg.dhTM4QDL0MTO0czW}`

<br><br>

## Challenge - 7 Grepping live output
This challenge is about teaching us about one of the bery important pipe command `|`
It redirects the output of one command into the input of some other command

for the challenge I redirect the output of /challenge/run into the grep command like this
`/challenge/run | grep pwn`

flag `pwn.college{QsSX8odtKMBEUl1ePSSLqVqcSay.dlTM4QDL0MTO0czW}`
<br><br>

## Challenge - 8 Grepping errors
The `|` only works when you want to redirect the standard output. It doesn't work when you want redirect stderr.
So for that to work you need to convert stderr into stdout using `2> & 1` and then pipe the output.

DFor the challenge what i do is I convert the error of /challenge/run into stdout tp pipe flag
`/challenge/run 2>& 1 | grep pwn`

flag `pwn.college{8y802FK8LAamaPbJK2jvLlynet7.dVDM5QDL0MTO0czW}`
<br><br>

## Challenge - 9 Duplicating piped data with tee
This one was kinda confusing.
it is used when you want to see what the command is outputing or what errors are being aroused while trasnfering of the output while it's still getting out.
So what you can do is `command | tee output_file_1 | output_file_2`
What it will do is, it will prouce the output of command in boht files while showing the output of file_1, so you can learn more about the internal working of your output

As for the challenge, `/challenge/pwn | tee check | /challenge/college`
It will show the output of /chalenge/pwn in check file, i.e, `/challenge/pwn --secret [SECRET_ARG]` with secret_arg being sDUfoxwy

`/challenge/pwn --secret sDUfoxwy | /challenge/college` gives the flag
flag `pwn.college{sDUfoxwyp_BPplyyJ1Mf8CbPsMD.dFjM5QDL0MTO0czW}`
<br><br>

## Challenge - 10 Writing to multiple programs 

<br><br>

## Challenge - 11 Split-piping stderr and stdout
<br><br>
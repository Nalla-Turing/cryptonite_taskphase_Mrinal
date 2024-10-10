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

## Challenge - 5 Redirecting input
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
This is a very imortant command that one must know. 
Here using chatgpt I learned that there is a major difference between `|` and `>`. It is that > is used to copy and transfer the output of a command to another file like text file. 
While | is used to trasnfer the output to a second command which will give the said output whenever called, while also maintaining copy of the output another file.

Now the question arises how we proceed when we want to trasnfer the output to two commands? Well for that we have something called *Process Substituion*.
What this process before tee works, it will create another pipe(or tunnel) that takes the output to the another >(command name) and gives the output. Now when used with multiple command, we will get different output as in accordance to different command effects.


For the challenge `/challenge/hack | tee >(/challenge/the) >( /challenge/planet )` gets the programm running.
Then It gives the output
    This secret data must directly and simultaneously make it to /challenge/the and
    /challenge/planet. Don't try to copy-paste it; it changes too fast.
    137791404183113478
    Congratulations, you have duplicated data into the input of two programs! Here
    is your flag:
    
    pwn.college{goN3hgy7-pk2yAnBXBFTdtP2_hW.dBDO0UDL0MTO0czW}

flag `pwn.college{goN3hgy7-pk2yAnBXBFTdtP2_hW.dBDO0UDL0MTO0czW}`
<br><br>

## Challenge - 11 Split-piping stderr and stdout
Ok this one was very confusing to complete the challenge I need to take the output from /challenge/hack and separate the stderr and stdout into 2 different commands.
My first thought was i can Process substitute the output into >(/challenge/planet) for stdout and 2>&1 (/challenge/the) for stderr but doesn't work as | tee only gets the stdout so there is no stderr to convert.

My next approach is to convert the stderr before hand then pass it to | tee but then it gives both the commands both output and error so it's a wrong method

After multiple tries of failing i chatgpted different ways the piping system works and found out that we can filter out stderr before hand using 2> and passing to >(/challenge/the)
and trasnfer the rest to | tee (/challenge/planet)

So I did `/challenge/hack 2> >(/challenge/the) | tee >(/challenge/planet)` and got the flag

flag `pwn.college{kBNB3hMBHE6G0372nfVsyQ_m-VW.dFDNwYDL0MTO0czW}`
<br><br>

Some extra that i learned 

Difference betwee > > and | tee >()

1st command takes the output and passs it to command in >() but | tee copies the output gives it to command >() and the other part to terminal to be printed or given to some other command.

`command | tee >(command1) >(command2) | command3 | command4`
How this will work is:-
It will create a output from command, divide that output into three parts and pass it to command1 command2 and command3. Then the output of command3 is copied and 1 part is given to command4 and the other to terminal.

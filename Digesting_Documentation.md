# Digesting Documentation
This module seems to be about trying to find the right place as to where to find help with your programs
<br><br><br>

## Challenge-1 Learing from Documentation
This challenge gives us a basic idea of reading ocumentation acan help us find the right specifications of our commands.

With the `/challenge/challenge` as the command the given documentation tells us `--giveflag` is the right argument

So using that, I get the flag
flag `pwn.college{ooFZDIDnfLWrHYxEXpiWrf53Z4J.dRjM5QDL0MTO0czW}`
<br><br>

## Challenge-2 Complex Usage
This challenge gives us an idea of how in some documentations we have information about commands which have aguments for arguements

So following the Documentation
`/challenge/challenge --printfile /flag` to get the flag
flag `pwn.college{wWnBNeOLsh43sMsudClT99aiJBT.dVjM5QDL0MTO0czW}`
<br><br>

## Challenge-3 Reading Manuals
Sometimes you don't need to search through internet to know more about the command
`man` is an inbuilt command that helps you find documentation about the command

The manual you get has the following parts
    NAME(1)                           CATEGORY                          NAME(1)

    NAME
	    This gives the name (and short description) of the command or
        concept discussed by the page.

    SYNOPSIS
	    This gives a short usage synopsis. These synopses have a standard
        format. Typically, each line is a different valid invocation of the
        command, and the lines can be read as:

	    COMMAND [OPTIONAL_ARGUMENT] SINGLE_MANDATORY_ARGUMENT
	    COMMAND [OPTIONAL_ARGUMENT] MULTIPLE_ARGUMENTS...

    DESCRIPTION
	    Details of the command or concept, with detailed descriptions
        of the various options.

    SEE ALSO
	    Other man pages or online resources that might be useful.

    COLLECTION                    DATE                          NAME(1)

Using the documentation, I used the command `/challenge/challenge --fortune` to know my fortune
Then use `/challenge/challenge --guvyyg 113` to get to the flag

flag `pwn.college{guvyNMyB1g1beKCVD3dpKd73GnD.dRTM4QDL0MTO0czW}`
<br><br>

## Challenge-4 Searching Manuals
This challenge is about some other methods to search specific items in the manual

`/` is for searching from front `?` is for back
`n` is to go to next result and `N` is for previous

Using the manual of challenge, we search for flag using \flag

and the use the new found command
`/challenge/challenge --knjztqe`

Flag `pwn.college{g5iaz6MgKkWO5SYaQ8qxCMdLD7A.dVTM4QDL0MTO0czW}`
<br><br>

## Challenge-5 Searching for Manuals
This module is about the cases when the the  information about your command may not directlty be given in such cases you need to other ways to find how to properly search for the command.

Now we can know more about the man techniques by doing `man man` command
:0

 Now using this and searchinf through the huge documentation for 10 minutes I found nothing. So I used chatgpt to find out that you can use

`man -k <keyword>` to find more about the keyword of your command
Doing that I found that `ypwcsoeffv` is where my challenge command is and it relates to printing the flag. `man ypwcsoeffv` gives us all about `/challenge/challenge` command

Now `/challenge/challenge --ypwcso 793` gives us the flag

flag `pwn.college{QMypw_cNs7oe93GFDffvfjyy36S.dZTM4QDL0MTO0czW}`
<br><br>

## Challenge-6 Helpful Programs
This Challenge is about teaching an alternative to `man` command as not every program might have man page.
But you learn how to run the man command using the
` |command| --help ` command. 
Here `help` can be replaced with `-h` `-?` `help` or `/?` but only when `--help` doesn't help

Now to complete the challenge I do `/challenge/challenge --help` getting the output
    usage: a challenge to make you ask for help [-h] [--fortune] [-v]
                                            [-g GIVE_THE_FLAG] [-p]

    optional arguments:
  - h, --help            show this help message and exit
    --fortune             read your fortune
    -v, --version         get the version number
    -g GIVE_THE_FLAG,   --give-the-flag GIVE_THE_FLAG
                          get the flag, if given the correct value
    -p, --print-value     print the value that will cause the -g option to
                          give you the flag

After doing `/challenge/challenge -p` and `/challenge/challenge -g GIVE_THE_FLAG ` I get the flag
flag `pwn.college{IbZoSGWuJ3G8jfXMmXwPJsERup1.ddjM4QDL0MTO0czW}`
<br><br>

## Challenge-7 Help for Builtins
Ratger than some commands with man pages or help informationn.
Theer are functions that are buily i the shell itself. These are called `builtins`

One can now more about the builtins by usig the `help` command or `help |command|` to know more about a specific builtin command.

To complete the challenge we do `help challenge` and get the information on  how to run the challenge command. Getting the flag

flag `pwn.college{IU34eyYLTusHXXFlhBpUL_7Ebg-.dRTM5QDL0MTO0czW}`
<br><br> 
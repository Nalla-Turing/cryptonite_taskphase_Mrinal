# Comprehending commands
This module is for some basic but very important commands used in Linux environment
<br><br><br>

## Challenge-1 Cat: not the pet, but the command!
`cat` command is one of the most used command used in linux , used to read files.

When given multiple arguments, cat command will concatenate the files and present them as one line at a time

So for the challenge I just added the ~/ directory before the flag file with cat command `cat ~/flag`

Flag:- `pwn.college{UtMZtvrT2k5lVx1VNOSz4d0Rbvw.dFzN1QDL0MTO0czW}`
<br><br>

## Challenge-2 catting absolute paths
Here we searching for the file in the absolute directory rather than jut hoping it already exists in our currently positioned home directory

`cat \file` is the command

Flag `pwn.college{0wHVQ7ryo5CBhFfK0mCrBuSK7Hb.dlTM5QDL0MTO0czW}`
<br><br>

## Challenge-3 more catting practice
Same stuff as before with just a new absolute path already given

Flag `pwn.college{UZJ5HO2mcpfxEQdmC3fak7vXrME.dBjM5QDL0MTO0czW}`
<br><br>

## Challenge-4 grepping for a needle in a haystack
Sometimes cat files can be very large, while we may need a single or multiple lines.
For such time we used `grep` command
It gives us the relevant line matching the pattern from a root file

The syntax is `grep <Options>(optional) <Pattern> File_name`

More about `grep` command in [here](https://docs.rockylinux.org/books/sed_awk_grep/2_grep_command/?h=grep)

For the challenge i do the command `grep pwn.college /challenge/data.txt`

Flag:- `pwn.college{QvZTEv0S9NYdiOTdcfJmasI_JsR.ddTM4QDL0MTO0czW}`
<br><br>

## Challenge-5 Listing files
Here learn to use the aforementioned `ls` command used to find contents inside a directory or a path

For the challenge I did `ls \challenge` to find the different files and then run the command after finding it

Flag `pwn.college{09D_QR_woFg9cKODMKABWi8UowT.dhjM4QDL0MTO0czW}`
<br><br>

## Challenge-6 Touching files :0
Here we learn to make new files using `touch` command.
Can be used to make files in  the current file or in a path
Commands were simple, nothing special needed

Flag:- `pwn.college{kH4QtesRtQT1ICQq0JBw_JCWCO6.dBzM4QDL0MTO0czW}`
<br><br>

## Challenge-7 Removing Files
`rm` command is used to remove files

`ls` command to check the contents and then `rm` command to run it

Flag:- `pwn.college{oQ74hBny-1vv8AKZMX4HfMkc3SJ.dZTOwUDL0MTO0czW}`
<br><br>

## Challenge-8 Hidden files
`ls` doesn't show all the files in a directory.
files starting with `.` will be saved as a hidden file.To see them u need to use the command `ls -a directory`

For the challenge do `ls -a /` to find the hidden directories in / and then use `cat` with file to gte your key

File:- `pwn.college{4qEIRxPPtwU0iV7DgFKkpbk9-Gh.dBTN4QDL0MTO0czW}`
<br><br>

## Challenge-9 An Epic FileSystem Quest
So this one is taking is taking a time consuming but here we go.
As the hint suggested, i canged my directory to `cd /`, taking me to the base of this drectory.
Then using `ls -a` to look for all the files present in the directory I found the TRACE file and `cat TRACE` gave me the next directory `The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Gyre-Pagella/Arrows`

Entering the directory, I agin `ls -a` to find the items in  the direvtory finding the WHSIPER file which i `cat` to find the next set of clues giving me the next directory and a hint ` the file starts with .`

Using the same methods as before the set of clues i get is
    Yahaha, you found me!
    The next clue is in: /opt/pwndbg/.venv/lib/python3.8/site-packages/sortedcontainers-2.4.0.dist-info

    The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.

They asking me to do the same thing i had been doing so far.Next step I found bunch of files but nothing that says clue. So idecide to `cat` every file one at a time. Luxcky I got DOSSIER had the clue. Next clue
    The next clue is in: /usr/share/racket/pkgs/htdp-doc/teachpack/htdp

    Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!

Ok so i an't cd into the directory, but I cansee what's in the directory just from here. So i do `ls /usr/share/racket/pkgs/htdp-doc/teachpack/htdp`, I find the clue as CUE-TRAPPED, so i access the file using the entire directory like `cat /usr/share/racket/pkgs/htdp-doc/teachpack/htdp` and I get the clue. 

Few more steps identical to these ones and I get the flag.

Flag `pwn.college{Ap7VHV6dFQA84FX2QLvMqZ8Q6As.dljM4QDL0MTO0czW}`
<br><br>

## Challenge-10 making directories
We learn that `mkdir` is used to make new directory inside your current directory
NOw to complete the challenge we have to create a new directory inside a directory temp
So as mentioned i jsut use `mkdir /tmp/pwn`
and then `touch /tmp/pwn/college` to complete the challenge.

Flag `pwn.college{crxGzgt2-oW9p3gC2yAs2eW7--U.dFzM4QDL0MTO0czW}`
<br><br>

## Challenge-11 findig files\
OK this was a good one had me at grip for a while
Now as the hint suggested I started with doing

`find -name file`
expecting it to search file in every directory in the filesystem, but got the no such directory output.
On searching it turns out when given with no location, by default it only searches starting in the current directory.

Chatgpt'ed the find command and found `/` argument is what is should use

Used `find / -name flag` to find all the flag files startig from root directiry.
got this output
![Alt Text](image.png)

Now comes the confusin part. I try find if any of the directories have the flag by writing `ls /directioyr`.
Some of the directories have some fkag name files with .c .o or .py extension
Tried to run them but quickly found out that's the worng approach.
So again used chatgpt'ed the function to find out the type of directory i have

It's the `file` function
So i use it on each directory and found the file directory with the txt extension
    /usr/share/help/ru/flag: ASCII text, with no line terminators

Now used ` cat /usr/share/help/ru/flag`

flag `pwn.college{AcjcGvYDg3hYEHzjfL2cTNAXfKh.dJzM4QDL0MTO0czW}`
<br><br>

##
<br><br>
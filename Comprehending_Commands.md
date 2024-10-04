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
Same stuff as before with just a new absolute path laready given

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
<br><br>

##
<br><br>

##
<br><br>

##
<br><br>

##
<br><br>
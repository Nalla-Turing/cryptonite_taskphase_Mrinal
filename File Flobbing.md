# File Globbing
In this module we learn about a new method of referencing our files without the need to tyoe out the entire the entirre path.
The method is callled *GLOBBING*
<br><br><br>

## Challenge - 1 Matching with *
The first glob is `*`. It's fucntion to output every match available that matches the pattern * has been used with

To complete the challenge, I do `cd /ch*` and it takes me to the challenge directory.
`/challenge/run` gets me the flag

flag `pwn.college{gCbV6A6CpJvp2z06wEs7f8b6Mrx.dFjM4QDL0MTO0czW}`
<br><br>

## Challenge - 2 Matching with ?
The next glob that is `?` is a specialized form of `*` as it only outputs the filename/directory that matches the pattern used with the name and has the same numbe of missing characters  as the number of ?

To complete the challenge. I typed `cd /?ha??enge` and got into the directory and eventually the flag

flag `pwn.college{YhtTmWXBTdhdRJmHe4NAnn9VtsG.dJjM4QDL0MTO0czW}`
<br><br>

## Challenge - 3 Matching with []
[] is a even more specialized form of ?. As inside [] you specify the differetn charcters you shell to check for.

For the challenge change directory `cd /challenge/files`
Then `/challenge/run file_[absh]` gives the flag

flag `pwn.college{A0X4N8rXu6opXH713ky0PDMQmUG.dNjM4QDL0MTO0czW}`
<br><br>

## Challenge - 4 Matching paths with []
`[]` can be used to for the entire path

For the challenge I did `/challenge/run /challenge/files/file_[absh]`

flag `pwn.college{IgyGneGMbspLxaPAe1ha23gcrV7.dRjM4QDL0MTO0czW}`
<br><br>

## Challenge - 5 Mixing globs
For the challenge we have to test the knowledge of the globbin we got.
So to complete the challenge what I do is `cd /challenge/files` and then `ls -a` to find all the files

Then to get them out i need to see a pattern. What i see is starting letter c,e,p is unique to them 
 `/challenge/files$ /challenge/run [cep]*` gets the flag

 flag `pwn.college{A8-0optRrCcoJHoh9iWby8kqu51.dVjM4QDL0MTO0czW}`
<br><br>

## Challenge - 6 Exclusionary globbing
In the [] you can add `!` or `^` in he beginning to exclude all the elements matching the inputs in a glob bracket

For the challenge
`cd /challenge/files` to get into the directory and

` /challenge/files$ /challenge/run [^pwn]* ` gets the flag

flag `pwn.college{cWDwIWzo_Kihoh__l3oy6qwz9ep.dZjM4QDL0MTO0czW}`
<br><br>
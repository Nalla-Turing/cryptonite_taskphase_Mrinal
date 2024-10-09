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

<br><br>

## Challenge - 5 Mixing globs
<br><br>

## Challenge - 6 Exclusionary globbing
<br><br>
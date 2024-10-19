# Untangling Users
This module takes us deeper into the users rabbit hole. Still  traumatised by previous module ke challenges
<br><br><br>

## Challenge- Becoming root with su
In this challenge, we need to use `su` to switch our user to `root`. 
`su` asks for the root password which in this case is `hack-the-planet`. 

After becoming root user, the flag can be read using `cat /flag`

flag `pwn.college{c8iAFTjOiTjHGEwAb-JapMbR4zE.dVTN0UDL0MTO0czW}`
<br><br>

## Challenge-2 Other users with su
This module is about teaching how to get access to some other user than root using the same `su` command

In this challenge, we need to switch to the user `zardus`instead. 
This can be done with `su zardus` and the password is `dont-hack-me`. 
Now `/challenge/run` gives

flag `pwn.college{kVeqF2TfyJu2WyxY5za5wLnVeh7.dZTN0UDL0MTO0czW}`
<br><br>

## Challenge-3 Cracking passwords
Here goes some actual hacking begins :)

A leak of `/etc/shadow` exists in `/challenge/shadow-leak`. It can be cracked using `john /challenge/shadow-leak` which gives the following output:

    Created directory: /home/hacker/.john
    Loaded 1 password hash (crypt, generic crypt(3) [?/64])
    Press 'q' or Ctrl-C to abort, almost any other key for status
    aardvark         (zardus)
    1g 0:00:00:18 100% 2/3 0.05387g/s 313.7p/s 313.7c/s 313.7C/s Johnson..buzz
    Use the "--show" option to display all of the cracked passwords reliably
    Session completed

Now you can used the password `aardvark` with `su zardus`
` /challenge/run` gives the flag

flag `pwn.college{QyUNyH6BkMgLrhCGcjBXH83oZeO.ddTN0UDL0MTO0czW}`
<br><br>

## Challenge-4 Using sudo
We cannot run `cat /flag` since we do not have superuser permission.

Since we have sudo permission, `sudo cat /flag` works and gives the flag

flag `pwn.college{MrGjmRh106YkRsdHTqBouCDP7_S.dhTN0UDL0MTO0czW}`
<br><br>
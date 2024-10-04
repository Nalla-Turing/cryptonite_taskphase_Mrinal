# Pondering Paths Writeup
From what i understand, this module is about learning the various ways we can understand path and directories that are used in while working iwth linux
<br><br><br>

## Challenge-1 The Root
We start our module by learning where it all begins. `/` is the root. 

As we go deeper into the directories, we spearate each level using this.
For this challenge I used the root to access the `pwn` program and got the flag below

`pwn.college{4icCgJ0n8WkIvoGHKV_wyelU757.dhzN5QDL0MTO0czW}`
<br><br>

## Challenge-2 Program and absolute Paths
Now we towards a bit complex paths. Now we are trying to reach the run program that lives in the challenege directory

So to acces it. what we do is, from our current base position we use `/` to go in the challenge `directory`.

Then we use `/` again to go in the challenge directory and access the `run` program
Effectivel making the entire path as `/challenge/run`, giving me the flag

`pwn.college{wCy-v3jle_WlnGhHmg3kq6fsoM0.dVDN1QDL0MTO0czW}`
<br><br>

## Challenge-3 Position thy self
OK so here we are to find a way to change the directory to our `/challenge/run` path is located

My first thought process was to find what is our current directory. As written in the position thy self
So as one does i chatgpt the command to find what our current directoy is? `pwd` is the command and i find the the path is `/home/hacker`

so i change the path to `cd /home` and then try to `/challenge/run`. It fails and asks me to find the `/var` directory

I change to `cd /var` to find the place

Flag `pwn.college{gb0z_XkzGjufRmHiUjN85-te0RN.dZDN1QDL0MTO0czW}`
<br><br>

## Challenge-4 Position elsewhere
This challenge is similar to last ones. Since it says the poistion elsewhere. I will try to hit and trial.
I do that and find that the path is same as before

Flag `pwn.college{0jR3N7yIoNp9FwfdgPnjQcqYVyg.ddDN1QDL0MTO0czW}`
<br><br>


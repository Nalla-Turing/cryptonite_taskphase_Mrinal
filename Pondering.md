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

## Challenge-5 Position yet elsewhere
Challenge was same as before, thus done in the same way

Flag `pwn.college{c9gi4uuKAXXG6HwQDjPif89DYNu.dhDN1QDL0MTO0czW}`
<br><br>

## Challenge-6 Implicit relative Paths
source -  Chatgpt
Implicit path are the path directories that start from your current directory itself.
It totally depends on your `current working directory (cwd)`.So rather than you starting from the absolute root `/` you can directly command the cmd to start from the directory name itself

For the challenge I move the the directory to / and then write the `challenge/run` command. Allowing me to inititae the command without using the absolute path

Flag `pwn.college{wJmL-UanGRk_NeScg1QsnOKFEQE.dlDN1QDL0MTO0czW}`
<br><br>

## Challenge-7 Explicit relatives paths
As shown in the given information what i understood was we have to go to the proper directory and `.` implicit entry to command our terminal to use the current directory to run the program we ask it to

So i go to `cd /` directory

Then i go to use `./challenge/run` to ask terminal to complete the challenge

Flag `pwn.college{0Gr5aUjN1_EQxkAHACZdj302ASP.dBTN1QDL0MTO0czW}`
<br><br>

## Challenge-8 implicit relative path
Here we learn about a very important safety measure in Linux.
Whenever we try to use naked programs in our directory, it rather than searching in the current directory searches up from the first layer directory.

> `#FFA500` why is important?
> `#FFA500` Because if there is some other file with the same name as what we want to run in a upper layer, it will execute in place of what we want

So for the solution change directory `cd /challenge`
then `./run` to run the command in the challenge directory itself

Flag `pwn.college{IGUjlJUI5kWbfxGT48Giicqi7mW.dFTN1QDL0MTO0czW}`
<br><br> 
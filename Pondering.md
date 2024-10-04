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
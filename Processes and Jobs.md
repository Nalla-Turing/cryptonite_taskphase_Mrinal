# Processes and Jobs
<br><br><br>

## Challenge-1 Listing Processes
In this challenge `/challenge/run` is renamed to something random and `ls` cannot be used in /challenge

The new /challenge/run process is already running so using `ps -ef` would show the new name of the process.
On running ps -ef the output is: 

    UID          PID    PPID  C STIME TTY          TIME CMD
    root           1       0  0 16:13 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /run/dojo/bin/sleep 6h
    root           7       1  0 16:13 ?        00:00:00 /run/dojo/bin/sleep 6h
    root          68       1  0 16:13 ?        00:00:00 /challenge/10730-run-24901
    root          72      68  0 16:13 ?        00:00:00 sleep 6h
    hacker        73       0  0 16:13 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint
    hacker        96      73  0 16:16 pts/0    00:00:00 ps -ef

On using the command `/challenge/10730-run-24901` the flag we get is

flag `pwn.college{U7P_2O9-Ber8ggGDML8Aw-rEQDT.dhzM4QDL0MTO0czW}`
<br><br>

## Challenge-2 Killing Processes
This challenge teaches us about killing previously running processes that might be hurting the current process
`/challenge/dont_run` must be killed before `/challenge/run` is executed so you get the flag.

The `PID` of `/challenge/dont_run` is found by using the `ps` command by: `ps -ef | grep /challenge/dont_run`

This gives the output:
![Image1](Image_resources\Img1.png)

The process is killed using `kill` by `kill 73`

Now running `/challenge/run` gives the flag
flag `pwn.college{M8LsAffQOikaNTnlxo_t4WzJMSn.dJDN4QDL0MTO0czW}`
<br><br>

## Challenge-3 Interrupting Processes
flag ``
<br><br>

## Challenge-4 Suspending Processes
flag ``
<br><br>

## Challenge-5 Resuming Processes
flag ``
<br><br>

## Challenge-6 Background Processes
flag ``
<br><br>

## Challenge-7 Foreground Processes
flag ``
<br><br>

## Challenge-8 Starting Background Processes
flag ``
<br><br>

## Challenge-9 Process Exit Codes
flag ``
<br><br>

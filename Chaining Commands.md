# Chaining Commands
Now this module..... This starts the real deal
Module about chaining several commands together

## Challenge-1 Chaining with Semicolons

`/challenge/pwn` and `/challenge/college` need to be chained together using `;`. This can be done using `/challenge/pwn; /challenge/college`, This gives 

flag `pwn.college{wx6e9YKhJdCKjd3geeOibj3VjZo.dVTN4QDL0MTO0czW}`

## Challenge-2 Your First Shell Script
Finally gonna start with my first file script yayyyy :D

The file `x.sh` is created using `touch x.sh`

I edited it using `nano` with `nano x.sh` and put the commands
```
/challenge/pwn
/challenge/college
```

Now this shell script is run using `bash x.sh`, this gives 

flag `pwn.college{8CEGAXNjTHlaSpjwDCytYKPIicB.dFzN4QDL0MTO0czW}`

## Challenge-3 Redirecting Script Output

The output from `x.sh` in the previous challenge must be piped to `/challenge/solve`. this can be done by `bash x.sh | /challenge/solve`, this gives 

flag `pwn.college{ckeeBcB6nwoGknb66__o-1Xdkd9.dhTM5QDL0MTO0czW}`

## Challenge-4 Executable Shell Scripts

A script `y.sh` that contains `/challenge/solve` is made.
I make it executable using `chmod +x y.sh`
Running it using `./y.sh` gives the 

    hacker@chaining~executable-shell-scripts:~$ touch y.sh
    hacker@chaining~executable-shell-scripts:~$ nano y.sh
    hacker@chaining~executable-shell-scripts:~$ chmod +x y.sh
    hacker@chaining~executable-shell-scripts:~$ ./y.sh
    Congratulations on your shell script execution! Your flag:
    pwn.college{AQl3Vs-_6hGQrJQwqBKbJyINUQL.dRzNyUDL0MTO0czW}

flag `pwn.college{AQl3Vs-_6hGQrJQwqBKbJyINUQL.dRzNyUDL0MTO0czW}`
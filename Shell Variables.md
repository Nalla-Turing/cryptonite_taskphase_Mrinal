# Shell Variables
This module starts wiht telliing us about command line on which we work is called Shell. And all our wriiten command is called Shell Scripts. This module  is about working with the Scripts.
<br><br><br>

## Challenge-1 Printing Variables
The module starts with teaching us what how variables can be printed???

    First a variable is a symbolic name that represents a value. It can store data, such as strings, numbers, or file paths, that can be used later in commands or scripts.

We use `$` before printing the variable so that our terminal prints the value that is inside the variable and not the name of varibale

We print the value using `echo` command.

For the challenge you need to print the flag stored in variable `FLAG` using `echo`. The value in the variable can be accessed using `$` prepended to it.
Flag `pwn.college{o5_IxJADZCDbz2ORIUDMjEHYMUm.ddTN1QDL0MTO0czW}`
<br><br>

## Challenge-2 Setting Variables
Just like reading you can also write values to a variable. You can do that using `=`.

The syntax being `<Var_name>=<Value>`
Make sure that there is no gap before or after =, as that will force shell to treat Var_name as a function.

`PWN` needs to be set to `COLLEGE` to get the flag for completing the challenge. This can be done by entering `PWN=COLLEGE` to the shell

Flag `pwn.college{gnDrC70fBhs7AXQhdrSldjm8Fj9.dlTN1QDL0MTO0czW}`
<br><br>

## Challenge-3 Mutli_word Variables
This challenge is about teaching how you can add multi worded value to a variable as normally shell sees the space and treat as a end of argument symbol.

To go around this we use `""` to store our value.

Similar to the previous challenge, but `PWN` must be set to `COLLEGE YEAH` which is two words. This can be achieved using `""` around COLLEGE YEAH

Therefore, `PWN="COLLEGE YEAH` which outputs the flag

Flag `pwn.college{QKm0VAvZORK1omhuR8xNTrFik7X.dBjN1QDL0MTO0czW}`
<br><br>

## Challenge-4 Exporting Variables
You can use user defined only in your current shell process. But in case a new shell process using commands like `sh` it won't work.

This security measure is put so that your information don't get leaked into other process unless you want to.

To yuse your variables in other processes, you need to export the variable first using `export` command.

First `PWN` is set to `COLLEGE` and exported using `export PWN=COLLEGE`

Then `COLLEGE` is set to `PWN` but not exported using `COLLEGE=PWN`

Then a child shell is invoked using `sh`

`/challenge/run` is run using arguments `PWN` and `COLLEGE`
<br><br>

## Challenge-5 Printing Exported Variables
use `env` commaqnd which prints out all the exported out variables. 

So for the challenge we use the `env` comand, and find the `FLAG` variables.

flag `pwn.college{8bFATuZh9k-f3KbxiFaSyjR5emR.dhTN1QDL0MTO0czW}`
<br><br>

## Challenge_6 Storing Exported Output
The output of `/challenge/run` can be stored in `PWN` using `PWN=$(/challenge/run)`

The flag is retreived by `echo PWN` which gives the output

flag `pwn.college{QtzLicYPPKod-VtNppJ5Gqs8rYq.dVzN0UDL0MTO0czW}`
<br><br>

## Challenge-7 Reading Input
This module teaches us about how to input form the user using the `read` command.

    You can also use -p argument to add a readbale strinf before your input for user experience  
`COLLEGE` has to be read from the input by the user and put in variable `PWN`

Input is read to PWN by `read -p "PWN is " PWN`

Now I type `COLLEGE` and enter, this outputs the flag

flag `pwn.college{kw4wLhcD7FEjzvGALk1o0RIbwAk.dhzN1QDL0MTO0czW}`
<br><br>

## Challenge-8 Reading Files
`/challenge/read_me` must be read to variable `PWN` to get the flag

This can be done by using `<` from the previous module

`read PWN < /challenge/read_me`

flag `pwn.college{k0Jd5-zeaIKnrVrOSkMf-wtAHhH.dBjM4QDL0MTO0czW}`
<br><br>
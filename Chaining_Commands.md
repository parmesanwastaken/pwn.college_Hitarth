# Chaining with Semicolons
I was asked to run 2 commands in one input

## My solve
**Flag:** `pwn.college{QnEXbx-6umppP4tx6qieWhXB7de.QX1UDO0wSO2EzNzEzW}`

- I simple used `;`
- Thus I ran: `/challenge/pwn; /challenge/college`

## What I learned
- I learnt I can use `;` to chain commands

## References 
Referred text given in challenge

---

# Building on Success
I was asked to run 2 commands using `&&` operator

## My solve
**Flag:** `pwn.college{YwLkAgPBig2eJDrqfgH9CQyqEZZ.0lM0MDOxwSO2EzNzEzW}`

- I typed `/challenge/first-success && challenge/second`

## What I learned
- I learnt to use `&&`
- It first checks whether first code ran or not, then only the other code is executed

## References 
Referred text given in challenge

---

# Handling Failure
I was asked to run 2 co..ands using `||` operator

## My solve
**Flag:** `pwn.college{EWuzn0-n87QxuZbiGCzXjEjz8SV.01M0MDOxwSO2EzNzEzW}`

- I typed `/challenge/first-failure || challenge/second`

## What I learned
- I learmt how to use `||` operator
- This only lets second command run if first one fails

## References 
Referred text given in challenge

---

# Your First Shell Script
Challenge asks me to do the first challenge but run it through a bash script this time

## My solve
**Flag:** `pwn.college{0JpzvNm-pTFIhlBODwedDwA8xlf.QXxcDO0wSO2EzNzEzW}`

```bash
hacker@chaining~your-first-shell-script:~$ echo "/challenge/pwn; /challenge/college" > x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
```
- This way it first saves both commands in `x.sh`
- Then I run it through `bash`

## What I learned
- I learnt how to write a bash script

## References 
Referred text given in challenge

---

# Redirecting Script Output
I was asked to create a script with 2 commands then pipe its output to another command

## My solve
**Flag:** `pwn.college{oZklAn1lqfNLAtWJqX5gK-aAldH.QX4ETO0wSO2EzNzEzW}`

```bash
hacker@chaining~redirecting-script-output:~$ echo "/challenge/pwn; /challenge/college" > test.sh
hacker@chaining~redirecting-script-output:~$ bash test.sh | /challenge/solve
Correct! Here is your flag:
```
- First I echoed both commands with semicolon into a shell script
- Then I piped it using `|`

## What I learned
- Revision of piping and creating script files
- So basically how to pipe a script output

## References 
Referred text given in challenge

---

# Executable Shell Scripts
I am asked to create a shell script and then make it executable

## My solve
**Flag:** `pwn.college{cvVmI9XGx4F-3EN8Me0BiTl4w8M.QX0cjM1wSO2EzNzEzW}`

```bash
hacker@chaining~executable-shell-scripts:~$ echo /challenge/solve > script.sh     hacker@chaining~executable-shell-scripts:~$ chmod +x script.sh
hacker@chaining~executable-shell-scripts:~$ ./script.sh
Congratulations on your shell script execution! Your flag:
```
- First I created a shell file
- Then I used `chmod` with `+x` to make the shell script executable
- Then I simply ran it with `./script.sh`

## What I learned
- I learnt how to make a shell script executable
- This makes running scripts easier instead of using `bash` all the time

## References 
Referred text given in challenge

---

# Understanding Shebangs
The challenge asks me to create a shell script with shebang and output a particular text. Also make it executable

## My solve
**Flag:** `pwn.college{4TV29n3_3JQJiAmAojZCkPIoCiz.0VOzMDOxwSO2EzNzEzW}`

- First I used `nano solve.sh`
- Then I entered following content into it:
```bash
#!/bin/bash

echo "hack the planet"
```
- Then I made it executable using `chmod +x`
- Finally I ran `/challenge/run` to get the flag

## What I learned
- I learnt about what she bangs are
- I also learnt that linix doesn't check file extensions, instead it looks for headers of file
- Thus I learnt how to make scripts with shebangs

## References 
Referred text given in challenge

---

# Scripting with Arguments
I am asked to creaete a script such that when I input 2 arguments, then it outputs them in reverse order

## My solve
**Flag:** `pwn.college{gBVuGZJV5I9RaSi3md0rXtkW_tv.0VNzMDOxwSO2EzNzEzW}`

- First I used `nano solve.sh`
- Then added following text to the script:
```bash
#!/bin/bash

echo "$2 $1"
```
- Thus it first gave output for second input and vica versa for first input

## What I learned
- I learnt that I can use `$` followed by number of argument in a script as a placeholder for argument in input.

## References 
Referred text given in challenge

---

# Scripting with Conditionals
I am asked to create a script that outputs `college` when the user inputs `pwn` as argument

## My solve
**Flag:** `pwn.college{M4uAxLlCLInVb63U_hlMDAkuAgM.0lNzMDOxwSO2EzNzEzW}`

- I used `nano solve.sh`
- And typed the following:
```bash
#!/bin/bash

if [ "$1" == "pwn" ]
then
        echo "college"
fi
```
- This gives output `college` everytime the user inputs argument `pwn`

## What I learned
- I learnt proper syntax of `if` statements in shell scripts
- I also learnt usage of  `then` and `fi`

## References 
Referred text given in challenge

---

# Scripting with Default Cases
The challenge asks me to create a similar script as above challenge, but this time add a `else` statement too

## My solve
**Flag:** `pwn.college{4WHhTIjqnlDn5n-hgut1Il7uiZF.01NzMDOxwSO2EzNzEzW}`

- I ran `nano solve.sh`, and entered the following:
```bash
#!/bin/bash

if [ "$1" == "pwn" ]
then
        echo "college"
else
        echo "nope"
fi
```
- This makes use of `else`, `if`, `then` and `fi`

## What I learned
- I learnt how to use `else` and `if` statements together in a shell script

## References 
Referred text given in challenge

---

# Scripting with Multiple Conditions
I am asked to create a shell script that makes use of `if`, `elif` and `else`

## My solve
**Flag:** `pwn.college{w2bo6Rwmhq5BeZFvNIZ6U_3AWX4.0FOzMDOxwSO2EzNzEzW}`

- I ran `nano solve.sh`, and typed:
```bash
#!/bin/bash

if [ "$1" == "pwn" ]
then
        echo "college"
elif [ "$1" == "hack" ]
then
        echo "the planet"
elif [ "$1" == "learn" ]
then
        echo "linux"
else
        echo "unknown"
fi
```
- This makes use of everything as asked in the challenge

## What I learned
- I learnt how to make use of `if`, `elif` and `else` together

## References 
Referred text given in challenge

---

# Reading Shell Scripts
I am asked to read a shell script and thus figure out the flag

## My solve
**Flag:** `pwn.college{Ms9HPChP_SjIKoAtd8Vk15PgvYM.0lMwgDOxwSO2EzNzEzW}`

- First I used `cat /challenge/run`
- The script first read the variable from user input, then it checked if input was same as given in script, if true then it gives the flag
- So I echoed the input with pipe in it
```bash
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ echo "hack the PLANET" | /challenge/run
CORRECT! Your flag:
```

## What I learned
- This was a bit challenging at first, but after revising  `read`, I was able to figure out the solution
- I also learnt how to read a shell script

## References 
Referred text given in challenge

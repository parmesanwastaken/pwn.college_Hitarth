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
type what the challenge asks

## My solve
**Flag:** 

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
example triple ticks for bash
```

## What I learned
explain what you learned

## References 
Referred text given in challenge

---

# Scripting with Conditionals
type what the challenge asks

## My solve
**Flag:** 

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
example triple ticks for bash
```

## What I learned
explain what you learned

## References 
Referred text given in challenge

---

# Scripting with Default Cases
type what the challenge asks

## My solve
**Flag:** 

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
example triple ticks for bash
```

## What I learned
explain what you learned

## References 
Referred text given in challenge

---

# Scripting with Multiple Conditions
type what the challenge asks

## My solve
**Flag:** 

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
example triple ticks for bash
```

## What I learned
explain what you learned

## References 
Referred text given in challenge

---

# Reading Shell Scripts
type what the challenge asks

## My solve
**Flag:** 

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
example triple ticks for bash
```

## What I learned
explain what you learned

## References 
Referred text given in challenge

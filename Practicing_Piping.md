# Redirecting output
The challenge asks me to write the word `PWN` in `COLLEGE` using `>` operator

## My solve
**Flag:** `pwn.college{UlXaXQh_lXbEqEGjhXdqHqYtTH3.QX0YTN0wSO2EzNzEzW}`

- I connected dojo using SSH
- I used `echo` for this
- I typed `echo PWN > COLLEGE`
- This appended the word `PWN` in `COLLEGE`

## What I learned
- I learnt how to add stdout in a file
- I learnt I can use `>` to directly add output in any file I want

## References 
Referred text given in challenge

---

# Redirecting more output
The challenge asks me to append `stdout` of `/challenge/run` in `myflag`

## My solve
**Flag:** `pwn.college{wtKxdHH5Xvo7EctFDkbrXJDv32V.QX1YTN0wSO2EzNzEzW}`

- I typed `/challenge/run > myflag`
- The terminal displayed success
- Thus I used cat to read  `myflag` and got the flag

## What I learned
- I revised how to again append output of a command into another file

## References 
Referred text given in challenge

---

# Appending output
Challenge asks me to use `>>` instead of `>` to append first and second half both in same file

## My solve
**Flag:** `pwn.college{IQXWeuyjkiaB4CkJJhuCrXWd0Nn.QX3ATO0wSO2EzNzEzW}`

- I wrote `/challenge/run >> /home/hacker/the-flag`
- This wrote both first and second half in `the-flag`
- Then I used cat to get the flag

## What I learned
- I learnt how to use `>>` to append multiple `stdout` in same file
- This helped me to avoid truncation, which would've happened if I used `>`

## References 
Referred text given in challenge

---

# Redirecting errors
The challenge asks to redirect output and errors in two different files

## My solve
**Flag:** `pwn.college{IulIO4G9gZUaqhqB2SocimqKpwj.QX3YTN0wSO2EzNzEzW}`

- I wrote `/challenge/run 1> myflag 2> instructions`
- This redirected output to myflag and error to instructions

## What I learned
- I learnt how to seperate `stdout` and `stderr` and redirect them to seperate files
- I also learnt how I can use `1>` specifically for `stdout` and `2>` for `stderr`

## References 
Referred text given in challenge

---

# Redirecting input
The challenge asks me to first add value `COLLEGE` to file `PWN`. Then input `PWN` file to `/challenge/run`

## My solve
**Flag:** `pwn.college{E7xkVTVJGdwOU-GW3MYtfd3kv1s.QXwcTN0wSO2EzNzEzW}`

```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
```
This gave me the flag

## What I learned
- I revised how to redirect again
- I also learnt how to input from a file

## References 
Referred text given in challenge

---

# Grepping stored results
Challenge asks to redirect output, then use grep to get the flag from output

## My solve
**Flag:** `pwn.college{kRUzYCen_6Xu3WPtbIwvMj_UFy3.QX4EDO0wSO2EzNzEzW}`

- I wrote `/challenge/run > /tmp/data.txt `
- This gave me a success
- So I used grep as `grep pwn.college /tmp/data.txt`
- This gave me the flag

## What I learned
- I revised grep and redirection of `stdout`

## References 
Referred text given in challenge

---

# Grepping live output
Challenge asks me to use grep on a live output

## My solve
**Flag:** `pwn.college{AD_gTkVBQiLBsRB3-NJ-3de3s-u.QX5EDO0wSO2EzNzEzW}`

- I wrote `/challenge/run | grep pwn.college`
- This checked for flag in output, and gave me the string with flag

## What I learned
- I learnt how to use `|` (pipe)
- I also learnt how to use any command on live output (especially grep)

## References 
Referred text given in challenge

---

# Grepping errors
The challenge asks me to grep from live errors. This can't be done directly, so I am asked to redirect errors to output and pipe to use grep 

## My solve
**Flag:** `pwn.college{YGuQ2kMBRCjLMLqjujhc3IWeUyU.QX1ATO0wSO2EzNzEzW}`
- I wrote ` /challenge/run 2>&1 | grep pwn.college`
- This first redirected `stderr` to `stdout`
- Then `|` made this output to input for grep
- This gave me the flag

## What I learned
- I learnt how to use use `&` to convert `stderr` to `stdout`
- I also learnt that `|` only works for output and not errors, so we have to convert everything to use it properly

## References 
Referred text given in challenge

---

# Filtering with grep -v
The challenge asks me to use `grep` with flag `-v` to exlude particular characters, and output only strings without those characters

## My solve
**Flag:** `pwn.college{4dSs7klYa-XcNTiSKo09ZDXasQw.0FOxEzNxwSO2EzNzEzW}`

- I wrote `/challenge/run | grep -v DECOY`
- This grepped live output, and `-v` flag omitted results which had `DECOY` in the string.

## What I learned
- I learnt the usage of `-v` with grep and how to omit strings using it

## References 
Referred text given in challenge

---

# Duplicating piped data with tee


## My solve
**Flag:** `pwn.college{E_6Qn_5VCHiq-lZBe0DEzSEua4E.QXxITO0wSO2EzNzEzW}`

```bash
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | /challenge/college
Processing...
^C
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn |tee test.txt| /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat test.txt
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "E_6Qn_5V"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret E_6Qn_5V | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{E_6Qn_5VCHiq-lZBe0DEzSEua4E.QXxITO0wSO2EzNzEzW}
```

## What I learned
- I learnt how to use `tee` to get multiple redirections
- This makes debugging much simpler, especially when error is due to first command in piped inputs.

## References 
Referred text given in challenge

---

# Process substitution for input
Challenge asks me to compare output of two files

## My solve
**Flag:** `pwn.college{kE6lzcVFm-RpTvE5ELzDc0c2gY-.0lNwMDOxwSO2EzNzEzW}`

```bash
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
34a35
> pwn.college{kE6lzcVFm-RpTvE5ELzDc0c2gY-.0lNwMDOxwSO2EzNzEzW}
```

## What I learned
- I learnt that Linux follows the philosophy that "everything is a file"
- Thus we can create temp files while using commands

## References 
Referred text given in challenge

---

# Writing to multiple programs
Challenge asks me to output a command and use that as input in other 2 commands

## My solve
**Flag:** `pwn.college{IGQFRvpP5j1Avx3F9z7vh2DPlD-.QXwgDN1wSO2EzNzEzW}`

```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) |  /challenge/planet
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
```

## What I learned
- I learnt how to use output as multiple inputes for different commands
- More use cases of `tee`
- Also how to use >(command) properly

## References 
- Referred text given in challenge
- Also referred to [Unix Shell Redirection Guide](https://web.archive.org/web/20220629044814/http://bencane.com:80/2012/04/16/unix-shell-the-art-of-io-redirection/)

---

# Split-piping stderr and stdout
Challenge asks me to:
`
    /challenge/hack: this produces data on stdout and stderr
    /challenge/the: you must redirect hack's stderr to this program
    /challenge/planet: you must redirect hack's stdout to this program
`

## My solve
**Flag:** `pwn.college{kGc4NsMLtsKvi2cao-AwJcKwQIs.QXxQDM2wSO2EzNzEzW}`
- I entered `/challenge/hack > >(/challenge/planet) 2> >(/challenge/the)`
- This redicted output to `/challenge/planet` and error to `/challenge/the`

## What I learned
- I learnt how to combine everything and set output of a command then seperate `stdout` and `stderr` and use them as input for commands

## References 
Referred text given in challenge

---

# Named pipes
I am asked to create `/tmp/flag_fifo` FIFO and input output from `/challenge/run` 

## My solve
**Flag:** `pwn.college{ULgH7bqbaYEQXPXcibLRwreYyve.01MzMDOxwSO2EzNzEzW}`

- I wrote `mkfifo /tmp/flag_fifo`
- Then I typed `/challenge/run > /tmp/flag_fifo`
- I opened a new terminal
- Reconnected SSH
- Then cat'd flag_fifo

## What I learned
- FIFO stands for First in, First out
- Advantages of FIFO over normal files

## References 
Referred text given in challenge

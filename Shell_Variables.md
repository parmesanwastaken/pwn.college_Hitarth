# Printing Variables
Challenge asks me to print `FLAG` variable

## My solve
**Flag:** `pwn.college{UiA6_0FvoQf5TlaPHi_SN7MFaFm.QX3UTN0wSO2EzNzEzW}`

- First I connected my terminal to dojo using SSH
- Then I typed `echo $FLAG`
- This gave me the flag

## What I learned
- I learnt how to get output from a shell variable

## References 
Referred text given in challenge

---

# Setting Variables
I am asked to set variable `PWN` with value `COLLEGE`

## My solve
**Flag:** `pwn.college{0YNqaimMHEoZ2VWwCpoz54Kt5S-.QX5UTN0wSO2EzNzEzW}`

- Entering `PWN=COLLEGE` gives the flag

## What I learned
- I learnt how to set value to a variable

## References 
Referred text given in challenge

---

# Multi-word Variables
Set a multiword variable value

## My solve
**Flag:** `pwn.college{wXuxUAl2klJoSVb1VCu9QdZn_r7.QXwYTN0wSO2EzNzEzW}`

- I typed `PWN="COLLEGE YEAH"`
- The quotations are so that it takes it as one string instead of two seperate inputs

## What I learned
- I learnt how to setup multi word value to a variable

## References 
Referred text given in challenge

---

# Exporting Variables
I was asked to create 2 varibles and assign them values, but only export one variable

## My solve
**Flag:** `pwn.college{4D0DH928NHzcO1pV6u5kRpaOAaV.QXyYTN0wSO2EzNzEzW}`

- First I typed `PWN=COLLEGE`
- Then I exported using `export PWN`
- Then I created `COLLEGE=PWN` and didn't export it
- Then I ran `/challenge/run` to get the flag

## What I learned
- I learnt how to export a flag

## References 
Referred text given in challenge

---

# Printing Exported Variables
I was asked to use `env` command which shows all the exported variables

## My solve
**Flag:** `pwn.college{A-Kd1Rm9xtHrZJb-NGmB9s85iY2.QX4UTN0wSO2EzNzEzW}`

- Using `env` , I got output:
```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=f70108391d3d05723056411b2768fae0f77c336941e767441494909a3ae58434
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{A-Kd1Rm9xtHrZJb-NGmB9s85iY2.QX4UTN0wSO2EzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```
- This gave me the flag

## What I learned
- I learnt about `env` command which shows all exported varibles and their values

## References 
Referred text given in challenge

---

# Storing Command Output
I was asked to store output of a command in a varible then print that variable

## My solve
**Flag:** `pwn.college{ohswamTl3_A2amWavcXhkfwf2WF.QX1cDN1wSO2EzNzEzW}`

```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{ohswamTl3_A2amWavcXhkfwf2WF.QX1cDN1wSO2EzNzEzW}
```

## What I learned
- I learnt how to copy output of a command in a variable

## References 
Referred text given in challenge

---

# Reading Input
I am asked to use `read` to get input inside a variable

## My solve
**Flag:** `pwn.college{Qh1_dgZroiIdA61PNJkuro7u0CT.QX4cTN0wSO2EzNzEzW}`

```bash
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
```

## What I learned
- I learnt how to use `read` command to get input for a variable

## References 
Referred text given in challenge

---

# Reading Files
I was asked to input a file inside variable

## My solve
**Flag:** `pwn.college{YevT68yj4PP0N_CkBfSoXu6m1Xd.QXwIDO0wSO2EzNzEzW}`

- I wrote `read PWN < /challenge/read_me`
- This added input inside variable

## What I learned
- I learnt how to directly input a file inside a variable

## References 
Referred text given in challenge

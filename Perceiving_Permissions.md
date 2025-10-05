# Changing File Ownership
The challenge asks me to change owner, in order to access flag

## My solve
**Flag:** `pwn.college{ELzNZ5jnj2SS-a7CCcLpViQjQKa.QXxEjN0wSO2EzNzEzW}`

- First I typed `ls -l /flag`
- It showed root as owner so I used `chown hacker /flag`
- Thus hacker user became the owner, then I catted it and got the flag

## What I learned
- I learnt how to use `chown` to change owner of a file

## References 
Referred text given in challenge

---

# Groups and Files
I was asked to change group, in order to access flag file

## My solve
**Flag:** `pwn.college{g5-t2KGr1LaZvdwJjc8eq8cVkT3.QXxcjM1wSO2EzNzEzW}`

- First I typed `ls -l /flag`
- It showed root as owner so I used `chgrp hacker /flag`
- Thus hacker group became the owner, then I catted it and got the flag

## What I learned
- I learnt how to change group owner of a file using `chgrp`

## References 
Referred text given in challenge

---

# Fun With Groups Names
type what the challenge asks

## My solve
**Flag:** `pwn.college{Y8EDDVQ9cqK_F3prH2qGxPN4EHG.QXycjM1wSO2EzNzEzW}`

```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp22378) groups=1000(grp22378)
hacker@permissions~fun-with-groups-names:~$ chgrp grp22378 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
```

## What I learned
- I learnt how to properly use `id`
- Revision for `chgrp` command

## References 
Referred text given in challenge

---

# Changing Permissions
I am asked to use `chmod` to change permissions of `/flag` file

## My solve
**Flag:** `pwn.college{QQTDRqH_Ghn46RvJ5K89YntryKB.QXzcjM1wSO2EzNzEzW}`

- I used `chmod a+rwx /flag`, this gave everyone all perms
- Then I simply catted it and got the flag

## What I learned
- I learnt how to use `chmod`
- Also good revision on what `r`, `w` and `x` means 

## References 
Referred text given in challenge

---

# Executable Files
I was asked to convert `/challenge/run` to executable file

## My solve
**Flag:** `pwn.college{c2n0rEHZIc33aR6BAL203GXuHbH.QXyEjN0wSO2EzNzEzW}`

- I typed `chmod +x /challenge/run`
- Then I checked whether I actually got the perms or not using `ls -l /challenge/run`
- Then I simply executed it and got the flag

## What I learned
- I learnt how to make a file executable

## References 
Referred text given in challenge

---

# Permission Tweaking Practice
I was asked to change perms as instructed on terminal

## My solve
**Flag:** `pwn.college{Msb1msRxhX8NlVNEXesaKE0r591.QXwEjN0wSO2EzNzEzW}`

- I kept changing perms are instructed
- `chmod u-r,o-r /challenge/pwn`
- `chmod u+rx,g+x /challenge/pwn`
- `chmod g-x /challenge/pwn`
- `chmod o+rw /challenge/pwn`
- `chmod u-rw,o-rw /challenge/pwn`
- `chmod o+wx /challenge/pwn`
- `chmod g+x /challenge/pwn`
- `chmod u+r /challenge/pwn`

## What I learned
- Good practice for `chmod`

## References 
Referred text given in challenge

---

# Permissions Setting Practice
Asked to do more practice with `chmod` using `=` and `,`

## My solve
**Flag:** `pwn.college{cjg8VNWr71YEJUkZIRUhph91hht.QXzETO0wSO2EzNzEzW}`

- I set perms as instructed:
- `chmod u=r,g=wx /challenge/pwn`
- `chmod u=wx,g=wx,o=wx /challenge/pwn`
- `chmod u=wx,g=rw,o=wx /challenge/pwn`
- `chmod u=rwx,g=r,o=wx /challenge/pwn`
- `chmod u=-,g=rx,o=rx /challenge/pwn`
- `chmod u=rwx,g=r,o=x /challenge/pwn`
- `chmod u=-,g=rx,o=rx /challenge/pwn`
- `chmod u=x,g=rwx,o=x /challenge/pwn`

## What I learned
- I got more practice on `chmod`

## References 
Referred text given in challenge

---

# The SUID Bit
I was asked to add SUID to user executable perm

## My solve
**Flag:** `pwn.college{U7hSM5Q3d4wlnlRi9Np8ERVn4I0.QXzEjN0wSO2EzNzEzW}`

```bash
hacker@permissions~the-suid-bit:~$ ls -l /challenge/getroot
-rwxr-xr-x 1 root root 155 Jan 14  2025 /challenge/getroot
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root!
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
```

## What I learned
- I learnt about SUID
- I also learnt I can use `u+s` with `chmod` to set SUID

## References 
Referred text given in challenge

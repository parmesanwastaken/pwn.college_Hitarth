# Becoming root with su
I was asked to become root user using `su`

## My solve
**Flag:** `pwn.college{k0oNtBKwI7Gih_k-0XTkm9-tBKY.QX1UDN1wSO2EzNzEzW}`

- I wrote `su`
- Then I entered the password `hack-the-planet`
- Then I ran `ls /` cause that directory requires root perms
- I found flag file there
- I catted it and got flag

## What I learned
- I learnt how to get root perms
- Thus accessing lower level file system

## References 
Referred text given in challenge

---

# Other users with su
Challenge asks me to switch to a user called `zardus`

## My solve
**Flag:** `pwn.college{QNZFmvDFVPVrBQSYAO1gD8vhqLu.QX2UDN1wSO2EzNzEzW}`

- I typed `su zardus`
- Then entered the password given in challenge
- Then ran `/challenge/run`

## What I learned
- I learnt how to switch to some other user using `su`

## References 
Referred text given in challenge

---

# Cracking passwords
I am asked to use johntheripper to crack pass and use that to access a user

## My solve
**Flag:** `pwn.college{8WejJc7kg2LfD4IQcFMCA1sKgMs.QX3UDN1wSO2EzNzEzW}`

```bash
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Created directory: /home/hacker/.john
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04840g/s 281.8p/s 281.8c/s 281.8C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
```
- First cracked it using `john`
- Then accessed the user using `su` and ran `/challenge/run` to get the pass

## What I learned
- Learnt how people abuse hashes and hoe they can be cracked too

## References 
Referred text given in challenge

---

# Using sudo
I was asked to use `sudo` to get the flag

## My solve
**Flag:** `pwn.college{o_B4H1iX3m7FKZ8gSlEqF3rX_nR.QX4UDN1wSO2EzNzEzW}`

- First ran `ls /`
- Saw `flag` file in this directory
- Thus used `sudo` to cat it and get the flag

## What I learned
- Learnt how we switched from `su` to `sudo`
- Got decent knowledge of `sudo`

## References 
Referred text given in challenge

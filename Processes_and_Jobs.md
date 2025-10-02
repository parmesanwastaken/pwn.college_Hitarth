# Listing Processes
I was asked to find running process similar to `/challenge/run` using `ps`

## My solve
**Flag:** `pwn.college{4zUsW2xouSsuVuCPJBpkzBo7tJz.QX4MDO0wSO2EzNzEzW}`

- I used `ps -ef` to find all running processes:
```bash
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 07:21 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 07:21 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 07:21 ?        00:00:00 /challenge/23623-run-30145
root         135     132  0 07:21 ?        00:00:00 sleep 6h
hacker       137       0  0 07:21 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoint
hacker       143     137  0 07:21 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       152     143  0 07:21 pts/0    00:00:00 ps -ef
```
- Only one process was inside `challenge` dir
- So I copied the path and ran it to get the command

## What I learned
- I learnt how to check running processes in a terminal
- I also learnt I can add flag `-ef` or parameter `aux` to get verbose info
- Also if I don't want truncation in path, I can use `ww` next to flag/parameter 

## References 
Referred text given in challenge

---

# Killing Processes
I was asked to kill a program and then run `/challenge/run` to get the flag

## My solve
**Flag:** `pwn.college{kfpsp5YndGkvlN3LKreMvp_XU7L.QXyQDO0wSO2EzNzEzW}`

- I used `ps -ef`
- This gave me PID `135` for `/challenge/dont_run`
- Then I used `kill 135`
- Finally I ran `/challenge/run` to get the flag

## What I learned
- I learnt how to kill a running process
- Also revision for `ps` 

## References 
Referred text given in challenge

---

# Interrupting Processes
I was asked to stop a running process using `^C` or `ctrl+C`

## My solve
**Flag:** `pwn.college{QQtVoJY7WLhWC6cTnIJTqoOuLNK.QXzQDO0wSO2EzNzEzW}`

- I ran `/challenge/run`
- Then pressed `ctrl + c`
- This got me the flag

## What I learned
- I learnt to stop process using `ctrl + c`

## References 
Referred text given in challenge

---

# Killing Misbehaving Processes
type what the challenge asks me to kill decoy processes then run absolute path which will send flag to FIFO

## My solve
**Flag:** `pwn.college{ICumlK8sqHwugvCXjVjd0mbdHtb.0FNzMDOxwSO2EzNzEzW}`

- I ran `ps -ef | grep decoy`
- Then I got the PID and killed the program
- I created a new shell instance, reconnected ssh
- Then I waited for few seconds and ran cat on fifo
- It gave me the flag

## What I learned
- Revised FIFO
- Revised to kill programs and `ps`
- ~~Learnt to be patient~~ 

## References 
Referred text given in challenge

---

# Suspending Processes
Challenge asks me to send current process in background and thus run another process at the same time in current shell

## My solve
**Flag:** `pwn.college{A24IlHzVdsX-FuAzsu-Q_EUlAqE.QX1QDO0wSO2EzNzEzW}`

- I ran `/challenge/run`
- Then pressed `ctrl + z` to send it to background
- Then I again ran `/challenge/run` which gave me the flag

## What I learned
- I can send a running process to background using `ctrl + z`

## References 
Referred text given in challenge

---

# Resuming Processes
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

# Backgrounding Processes
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

# Foregrounding Processes
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

# Starting Backgrounded Processes
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

# Process Exit Codes
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

# cat: not the pet, but the command!
I am asked to check what's written in flag file in home directory

## My solve
**Flag:** `pwn.college{gyA7_ynDutkLrJ14lsJbq_Bgp83.QXxcTN0wSO2EzNzEzW}`

- First I had to connect to ssh
- Then I used cat command to check what's inside file named 'flag'
- So I wrote `cat flag` and got flag

## What I learned
- I learnt how to use cat command to check raw text inside files
- I also learnt that I can read multiple files through one cat command

## References 
Reference was just text written under pwn.college challenge

---

# catting absolute paths
I am asked to use absolute path for finding the flag

## My solve
**Flag:** `pwn.college{AA5LRLU_uYQH7RT04QvnbZ0zVCl.QX5ETO0wSO2EzNzEzW}`

- I used `cat /flag` to specify flag as an absolute path

## What I learned
- I learnt I can use absolute path with cat command, to read raw text from anywhere

## References 
Text in pwn.college challenge was referred.

---

# more catting practice
Challenge asks me to read file under `/lib/groff/flag`

## My solve
**Flag:** `pwn.college{wIQ7QXC9VpaNZ4AI650gTCfyzuV.QXwITO0wSO2EzNzEzW}`

- Terminal specified where file was
- It asked me not to cd into it
- So I used absolute path with cat to find flag
- I wrote `cat /lib/groff/flag`

## What I learned
- I learnt more about absolute path with cat command.

## References 
I referred through text in pwn.college challenge

---

# grepping for a needle in a haystack
I am asked to find flag inside a file which contains thousands of lines of text

## My solve
**Flag:** `pwn.college{gt2-oXD_QByzbP6cPzKv_0lFr0N.QX3EDO0wSO2EzNzEzW}`

- I know flag starts with pwn.college
- So I wrote `grep pwn.college /challenge/data.txt`
- This grabs the string which contains pwn.college text in it and gives me the flag

## What I learned
- I learnt how to use grep and use absolute path with it to find string containing specified text.

## References 
I just referred through text in challenge

---

# comparing files
type what the challenge asks

## My solve
**Flag:** `pwn.college{shjAKG3eqXSar6wiakUKqxaMZGK.01MwMDOxwSO2EzNzEzW}`

- I used `diff` with two absolute paths: `/challenge/decoys_and_real.txt` and `/challenge/decoys_only.txt`
- This gave me output:
```bash
  7d6
< pwn.college{shjAKG3eqXSar6wiakUKqxaMZGK.01MwMDOxwSO2EzNzEzW}
```
- This means a particular line was deleted from decoys only file

## What I learned
- I learnt how to use diff to check 2 files
- This helps us find differences in two files and gives us proper output in terms of a,d,c
- a means that a line is added, c means that it is changed, d means that it is deleted

## References 
- I referred text provided in challenge
- I also referrred basic linux wiki and man command to understand what the single characters in output means and different parameters in diff commands.

---

# listing files
I was asked to use ls command to find renamed name of run file in challenge directory

## My solve
**Flag:** `pwn.college{IiWujzyiqUwhoqxz_DhVzi1Hm3q.QX4IDO0wSO2EzNzEzW}`

- I used ls command with absolute path `/challenge` to find renamed name of run file
- Then I specified absolute path to find the flag by running run file `/challenge/10585-renamed-run-19227`

## What I learned
- I learnt how to use ls command
- It also works with absolute paths

## References 
Referred text given in challenge

---

# touching files
Challenge asks me to create two files named pwn and college then run file named run

## My solve
**Flag:** `pwn.college{0vf-YKPICii8F7H7k_Ph5AaWWoi.QXwMDO0wSO2EzNzEzW}`

- I cd'd into /tmp
- Then I created two files using touch
- Then I ran file using `/challenge/run`

## What I learned
-I learnt to create files using touch command

## References 
Referred text given in challenge

---

# removing files
Challenge asks me to delete file using rm

## My solve
**Flag:** `pwn.college{cxMtR8HtnMdL-lB-6v0yOO303ud.QX2kDM1wSO2EzNzEzW}`

- I used rm command to remove `delete_me` file
- Then I used absolute path to get flag

## What I learned
- I learnt how to use `rm` command to remove files

## References 
Referenced text in challenge

---

# moving files
I am asked to move a file from one directory to another

## My solve
**Flag:** `pwn.college{AMpalXBvU-TJdWSMW8J8m6mzpW8.0VOxEzNxwSO2EzNzEzW}`

- I used `mv` command to move files from /flag to /tmp/hack-the-planet


## What I learned
- I learnt how to use `mv` command to move files from one path to anothers

## References 
Referenced text in challenge

---

# hidden files
Challenge asks to find flag by finding hidden file in root folder

## My solve
**Flag:** `pwn.college{UDBJ7QOOwDUxnwHdB88khlqQadW.QXwUDO0wSO2EzNzEzW}`
- I cd'd to `/`
- Then I ran  `ls -a` to find all files
- Then I used cat to find flag inside `.flag-117021465411867` file

## What I learned
- I learnt how to use ls command to find hidden files through -a parameters

## References 
Referenced text in challenge

---

# An Epic Filesystem Quest
I was asked to find flag using `ls`, `cd`, `cat` and `-a` parameter

## My solve
**Flag:** `pwn.college{gY68j_5wXMSZ9wLLi-0bYvAq7Q9.QX5IDO0wSO2EzNzEzW}`

- First cd'd into ` /usr/local/lib/python3.8/dist-packages/pip/_internal/metadata/__pycache__`
- Then `cat SECRET`
- Then did `ls /usr/share/racket/pkgs/htdp-lib/typed/test-engine/compiled`
- Got files inside it so `cat /usr/share/racket/pkgs/htdp-lib/typed/test-engine/compiled/TEASER-TRAPPED`
- Then again `ls /usr/lib/python3/dist-packages/sympy/parsing`
- Which gave me files so I did `cat INSIGHT`
- Then I `ls -a /usr/lib/python3/dist-packages/mpmath/libmp`
- Then ran `cat /usr/lib/python3/dist-packages/mpmath/libmp/BLUEPRINT-TRAPPED`
- Then ls'd again with -a ~~(I hate this loop)~~ `ls -a /usr/share/racket/pkgs/typed-racket-lib/typed-racket/typecheck/tc-app/compiled`
- Then `cat /usr/share/racket/pkgs/typed-racket-lib/typed-racket/typecheck/tc-app/compiled/.HINT`
- Again did the whole loop for path `/usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/STIX-Web/Size5/Regular` and file `.GIST'`
- Then cat'ed the final file in `/usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/Asana-Math/MESSAGE-TRAPPED`

## What I learned
- Extensive knowledge on `cd`, `ls` and `cat`
- ~~How to annoy someone with stupid file loops~~

## References 
Just text in challenge

---

# making directories
It asked me to create a directory in root folder and a file inside it

## My solve
**Flag:** `pwn.college{YyVXyeaOZQGa-eGCQsivR_PLKDo.QXxMDO0wSO2EzNzEzW}`

- First I made a new directory using mkdir i.e `mkdir /tmp/pwn`
- Then I used `cd /tmp/pwn`
- Then I created a new file inside it using `touch college`
- Then I ran /challenge/run to get flag

## What I learned
- Revision for touch command
- how to use mkdir to make new sub directories

## References 
Just text in challenge

---

# finding files
The challenge asks me to find all the files in directory, then find flag file and find flag inside it

## My solve
**Flag:** `pwn.college{Up6F8g4F_OkiHEFlS7CEp8KS8en.QXyMDO0wSO2EzNzEzW}`

- First I ran `find / -name flag`
- Then it gave output and I pressed `ctrl +c` because it was taking too much time
- I got a file and used cat to read it
- This gave me the flag

## What I learned
- I learned to find files inside a directory
- How to find all files in /
- How to use -name to specify file name

## References 
Only text mentioned in challenge

---

# linking files
I was asked to use symlinking to execute a file

## My solve
**Flag:** `pwn.college{I-hu1XbXI1cMUqTKIlju747KdIu.QX5ETN1wSO2EzNzEzW}`
- I removed `not-the-flag` using `rm`
- Then I linked `/flag` using `ln -s /flag not-the-flag`
- Then I ran `./catflag`
- This gave me the flag

## What I learned
- I learnt how to use symlink
- I also learnt difference between soft and hardlink

## References 
- I referred given video
- I referred text in challenge
- I also referred basic linux wiki command to understand more about linking file systems

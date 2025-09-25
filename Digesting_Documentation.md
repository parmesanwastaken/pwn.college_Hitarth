# Learning From Documentation
The challange asks me to read a basic documentation provided in challenge and use flags with command based on that.

## My solve
**Flag:** `pwn.college{cuheXZE679_yI2z3q4-HNzIAM7e.QX0ITO0wSO2EzNzEzW}`

- First I connected to pwn.college dojo module using ssh
- I was asked to use flag `--giveflag` with absolute path `/challenge/challenge`
- So I invoked this using `/challenge/challenge --giveflag`

## What I learned
- I learnt how to understand basic documentation and use flags with commands
  
## References 
Referred text given in challenge on pwn.college

---

# Learning Complex Usage
Challenge gives me an example and brief documentation on how I can use `--printfile` argument with `/challenge/challenge` to printout a file. So I am asked to find flag using this.

## My solve
**Flag:** `pwn.college{MVK5MKgY5VOHF-y-19JGSM9A8Hb.QX1ITO0wSO2EzNzEzW}`

- I first used `/challenge/challenge --printfile /challenge/challenge`
- This doesn't give flag but I realised I was using the command properly
- I got really confused and tried to list out various directory with `-a` flag, but still couldn't find anything
- Then I remembered, there is usually a flag file in `/`
- So I wrote `/challenge/challenge --printfile /flag`
- This gave me the flag

## What I learned
- I learnt how to read more complex documentations, and thus use arguments with flags
- Also realised we did similar action with find command, which was a nice recap

## References 
Referred text given in description of challenge

---

# Reading Manuals
The challenge asks me to use man command to read documentation of challenge command

## My solve
**Flag:** `pwn.college{wx_EqE3ayxjpAAyZh42etQ7_BOA.QX0EDO0wSO2EzNzEzW}`

- I used `man challenge`
- This told me about `/challenge/challenge` command
- It also told me about `--wxqayx` flag which returns flag when I use `342` as argument with it

## What I learned
- I learnt about man command ~~(my fav command; only reason I am still alive after using fmmpeg lmao)~~
- I learnt how to properly read it and learn more about flags used with command through man pages

## References 
Referred description provided with the challenge

---

# Searching Manuals
Challenge asks me to man challenge command and thus find flag inside it

## My solve
**Flag:** `pwn.college{IRym39Li3OyNpzGkvHLPnkcwyGW.QX1EDO0wSO2EzNzEzW}`
- I used `man challenge`
- This told me I need to use `/challenge/challenge`
- I searched through man page with `/flag` to find the argument which gives flag
- Then I pressed `q` to go back
- Finally I wrote `challenge --yk` to get the flag

## What I learned
- I learnt how to search in man pages
- I can even use `n` and `N` to check next search result
- `/` is used to search from top to bottom and `?` is used to search from bottom to top

## References 
- I referred text provided in challenge
- I also used basic linux command wiki to properly understand differencce between `/` and `?` when searching through man pages

---

# Searching For Manuals
type what the challenge asks

## My solve
**Flag:** `pwn.college{helloworld}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
example triple ticks for bash
pwn.college{helloworld}
```

## What I learned
explain what you learned

## References 
Add any references or videos u used while solving the challenge.

---

# Helpful Programs


## My solve
**Flag:** ``


## What I learned
explain what you learned

## References 
Add any references or videos u used while solving the challenge.

---

# Help for Builtins
type what the challenge asks

## My solve
**Flag:** `pwn.college{helloworld}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
example triple ticks for bash
pwn.college{helloworld}
```

## What I learned
explain what you learned

## References 
Add any references or videos u used while solving the challenge.

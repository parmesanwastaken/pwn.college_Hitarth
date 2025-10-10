# The PATH Variable
I am asked to make it so /challenge/run cannot find `rm`, thus it gives me the flag and doesn't remove it

## My solve
**Flag:** `pwn.college{oCMHnbAKD4Zqa0-BZE-vs3LTEXj.QX2cDM1wSO2EzNzEzW}`

- I used `Path=""`
- This way the default commands like `rm` are not recognized
- Thus `/challenge/run` cannot remove the flag and gives me

## What I learned
- I learnt default commands are stored in `PATH`
-  Making `PATH` empty causes error 

## References 
Referred text given in challenge

---

# Setting PATH
I was asked to set a directory tas `PATH`

## My solve
**Flag:** `pwn.college{YheKuRo4XwJgNo5AFOQuOw7bjo4.QX1cjM1wSO2EzNzEzW}`

- I first did `PATH=""`
- Then added `/challenge/more_commands/` using `PATH="/challenge/more_commands/"`
- Then simply ran `/challenge/run` to get the flag

## What I learned
- I learnt I can set directories to PATH to directly run stuff from it, without always mentioning absolute path

## References 
Referred text given in challenge

---

# Finding Commands
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

# Adding Commands
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

# Hijacking Commands
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

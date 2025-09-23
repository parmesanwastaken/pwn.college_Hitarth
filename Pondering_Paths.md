# 1. The Root 
The challenge asks to invoke a program by providing its exact path. i.e I have to access root folder and invoke program in it.

## My solve
**Flag:** `pwn.college{ggEm9qrljDIOcAGEoqOdAefkqGj.QX4cTO0wSO2EzNzEzW}`

- First I connected to pwn.college through ssh
- Then I wrote / for root followed by pwn i.e `/pwn`
- This ran the pwn program inside root folder (/), thus I got the flag

## What I learned
- I learnt about file structure and how there exists a main folder called root
- Then there are sub directories or program inside the main root directory
- I also learn how to specify a specific path (absolute path) from start to define the location of a program and run it

## References 
- I went through video provided on pwn.college
- Also I looked through a flowchart to understand tree file structure and how different files are present inside subdirectories



# 2. Program and absolute paths 
The challenge asks to further go into another directory present in root and run a program inside it.

## My solve
**Flag:** `pwn.college{khwpbyCjv7cl31dXdOV9oI03WjE.QX1QTN0wSO2EzNzEzW}`

- First I connected to pwn.college terminal from my terminal through ssh
- Then I was asked to run a file inside subdirectory which is present in main root directory
- So I ran:
  ```bash
  hacker@paths~program-and-absolute-paths:~$ /challenge/run
  ```
- This ran a program called run inside challenge folder, which is inside root folder.

## What I learned
- From previous challenge I learn how to run a program inside root, but this challenge helped me to learn how to run a program further inside a directory
- This gave me more exposure to tree structure of linux file system
- Thus I learn how to access files present nested inside folders.

## References 
- I reffered the tree structure flowchart and video present on pwn.college

# 3. Position thy self
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



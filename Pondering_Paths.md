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
The challenge asks me to use cd command to change directory to a particular path as instructed

## My solve
**Flag:** `pwn.college{Y0D-3l9XuptomwwBAI4VaPpONtj.QX2QTN0wSO2EzNzEzW}`

- First I connected through ssh
- Then I ran /challenge/run
- It told me to go to /sys path
- I did cd to that path and ran /challenge/run which executed the program

## What I learned
I learnt how to change directory using cd ~~(although z [zoxide] is better, gotta use what I got)~~

## References 
I referenced the notes present on pwn.college and video linked on it



# 4. Postion elsewhere
The challenge asks me to change directory as instructed on terminal and then run /challenge/run

## My solve
**Flag:** `pwn.college{kjFNZf3MdUwGw7KZ6Jcc15FEn1o.QX3QTN0wSO2EzNzEzW}`


- First I connected through ssh
- Then I ran /challenge/run
- It told me to go to /usr/share/build-essential path
- I did cd to that path and ran /challenge/run which executed the program

## What I learned
I learnt how to change directory to even deeper path ~~(zoxide would've done it much easily)~~

## References 
I referenced the notes present on pwn.college and video linked on it



# 5. Position yet elsewhere
The challenge asks me to change directory as instructed on terminal and then run /challenge/run

## My solve
**Flag:** `pwn.college{oMy2iqewtjy0S_Tjif1Q0NeKhRF.QX4QTN0wSO2EzNzEzW}`


- First I connected through ssh
- Then I ran /challenge/run
- It told me to go to /usr/bin path
- I did cd to that path and ran /challenge/run which executed the program

## What I learned
I learnt how to change directory to yet another path ~~(stopping the zoxide glazing, but it would've fr been better)~~

## References 
I referenced the notes present on pwn.college and video linked on it


# 6. Implicit relative paths, from / 
The challenge first places me in a random directory and then asks me to run /challenge/run through implicit relative path

## My solve
**Flag:** `pwn.college{cwmpk9bXx4yY9Y64KeqBOeNVhSu.QX5QTN0wSO2EzNzEzW}`

- At first I checked my current path using pwd
- Then I used `cd /` to go to root folder
- Then I wrote `challenge/path` as it doesn't start with `/` so it is a relative path
- This gave me flag

## What I learned
I learnt how to use relative paths i.e how to execute programs inside a directory which are withing subfolders without mentioning the whole path from start

## References 
I referenced the text already provided in pwn.college challenge



# 7. Explicit relative paths, from /
The challenge askes me to use relative path that includes .

## My solve
**Flag:** `pwn.college{gcNVKK8x0r4IkLFmkWl-uvML2P9.QXwUTN0wSO2EzNzEzW}`

- First I used cd to go to root folder using `cd /` (Probably should've used cd .. instead to go back to parent folder)
- Then I used `./challenge/run` to run the run program
- This gave me flag

## What I learned
- I learnt that single period refers to current directory
- This can be used to run programs inside a directory, for eg. When I am in challenge directory I can run using `./run`
- I also learn that .. refers to parent directory, which can be used to go back easily

## References 
I refered through text given in pwn.college

# 8. Implicit relative path 
Challenge asks me to run a program inside directory when I am inside that directory

## My solve
**Flag:** `pwn.college{gYx2-00O5rxbdIvqZhjX_lwPCLv.QXxUTN0wSO2EzNzEzW}`
- I went to challenge directory using `cd /challenge`
- Then I wrote `./run` to run the program, the . is used so it knows that I am talking about this directory

## What I learned
- I learnt how to execute programs while I am inside the mentioned directory (although I unknowingly wrote the same usecase in challenge 8 writeup lol)

## References 
Reference was just the texet mentioned in pwn.college challenge



# 9. Home sweet home
The challenge asks me to mentioned `/challenge/run` at the start and then write a path following it with constrains:  

1. Your argument must be an absolute path.
2. The path must be inside your home directory.
3. Before expansion, your argument must be three characters or less.


## My solve
**Flag:** `pwn.college{8ZACf4O-sUS90JXiEpDquygWcKB.QXzMDO0wSO2EzNzEzW}`

- I wrote `/challenge/run ~/~`
- This means same as `/challenge/run /home/hacker/~`
- This way it uses just 3 characters, it is an absolute path and uses 3 characters.

## What I learned
- This was a nice last challenge to recap everything above
- I learn that using ~ twice just converts one ~ to home/user directory and other stays ~
- Also that cd uses home as one's default location
- Bash uses $ symbol to signify home/user, thus it is seen after ~ in prompt.

## References 
Reference was just text given in challenge

# Translating characters
I was asked to switch characters from capital to small and small to capital using `tr` from output of `/challenge/run`

## My solve
**Flag:** `pwn.college{cewvGhmnoC40dyfyXQxtWoq4WoJ.01MxEzNxwSO2EzNzEzW}`

- First I connected to DOJO using `ssh`
- I had to look into previous programs a bit, but I figured I can use a-z for a,b..z letters
- Then I looked around on internet for a while and realised I had to use `A-Za-z` to mention both capital and small characters
- Thus I used `/challenge/run | tr 'a-zA-Z' 'A-Za-z'`
- This switched upper case with lower case and visa versa

## What I learned
- The best thing I learnt was to mention upper case and lower case at the same time, as that was confusing me at first.
- I also learnt how to use `tr`
- Revised how to mention all alphabets by using `a-z`

## References 
- Referred text given in challenge
- Also referred bash manual
- Scoured few forums/threads online for mentioning both upper and lower case together

---

# Deleting characters
Challenge asks me to find flag from output of `/challenge/run` but it contains a lot of extra characters, which I am supposed to remove by `tr`

## My solve
**Flag:** `pwn.college{0F5p-cPSlLk62YyJV5rGNDdvJZE.0FNxEzNxwSO2EzNzEzW}`

- I just ran `/challenge/run | tr -d %^`
- At first I thought maybe I can use `![a-zA-Z0-9]`, but that doesn't work with `tr` apparently
- So as mentioned in challenge I just stuck with removing '%' and '^'

## What I learned
- I learnt how to use `-d` flag with tr to delete characters

## References 
Referred text given in challenge

---

# Deleting newlines
Challenge asks me to remove new line from output to get the flag

## My solve
**Flag:** `pwn.college{kU4L2hFVh6b0Xyai72uhN0u-VzR.0VNxEzNxwSO2EzNzEzW}`

- I got that `\n` means new line
- Also `-d` is used for deleting characters
- Thus I typed `/challenge/run | tr -d '\n'`

## What I learned
- I learnt that `\n` means new line
- Also if I wanna remove `\` then I will have to use `\\`
- Also revision on `tr` and `-d` flag

## References 
Referred text given in challenge

---

# Extracting the first lines with head
I was asked to use `head` command for first 7 lines and pipe it to `/challenge/college` to get the flag

## My solve
**Flag:** `pwn.college{4AdAw6NuOaH0FM0O6twsBzPPRC6.0lNxEzNxwSO2EzNzEzW}`

- I entered `/challenge/pwn | head -n 7 | /challenge/college`
- This first pipes `/challenge/pwn` to head, which mentions that only first 7 lines should be the output
- Then these 7 lines are piped to `/challenge/college`
- This outputs flag

## What I learned
- I revised piping
- I also learnt about `head` and using `-n` flag for specific number of lines

## References 
Referred text given in challenge

---

# Extracting specific sections of text
The challenge asks me to use `cut` to get flag characters and then pipe it through `tr` to remove new line and get flag

## My solve
**Flag:** `pwn.college{srGXCH9u4FblL6EDn5YG8GSJOAX.01NxEzNxwSO2EzNzEzW}`

- I first ran `/challenge/run`
- This gave me output:
```bash
25965 p
28046 w
11598 n
29057 .
21974 c
3775 o
12656 l
14157 l
16578 e
11911 g
18459 e
27838 {
16341 s
22458 r
12944 G
17692 X
20522 C
13915 H
11544 9
17359 u
25528 4
758 F
29335 b
13569 l
2578 L
13927 6
13534 E
24091 D
24987 n
12846 5
5900 Y
10263 G
6365 8
28424 G
5020 S
7876 J
27979 O
27312 A
19309 X
25649 .
20222 0
1594 1
28852 N
22193 x
548 E
4194 z
20986 N
4500 x
6044 w
13696 S
9492 O
22544 2
5515 E
23030 z
15152 N
20569 z
2752 E
25196 z
18864 W
31787 }
```
- This meant I had to use column delimiter as space and column number 2
- Then I piped it through `tr -d '\n'`
- Full command: ` /challenge/run | cut -d " " -f 2 | tr -d '\n'`
- This gave me the flag 

## What I learned
- I learnt how to use `cut`
- I also got decent revision on `tr` and piping

## References 
Referred text given in challenge

---

# Sorting data
Challenge asks me to sort and get flag from last line of output

## My solve
**Flag:** `pwn.college{Q75W0pJtnJ8H45AGNalhVxYtVjU.0FM0MDOxwSO2EzNzEzW}`

- I used `sort /challenge/flags.txt | tail -n 1`
- This sorted the file and piped it to `tail`, which I opposite of `head` and I mentioned only to give last output with `-n` flag
- Thus I copied the ouptput and got the flag
- Could've also used `-r` to get the flag as first output

## What I learned
- I learnt how to use `sort`
- I also learnt about various flags for `sort` command:

```bash

    -r: reverse order (Z to A)
    -n: numeric sort (for numbers)
    -u: unique lines only (remove duplicates)
    -R: random order!
```

## References 
Referred text given in challenge

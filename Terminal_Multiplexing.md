# Launching Screen
Challenge asks me to write `screen`

## My solve
**Flag:** `pwn.college{UM9a7JQH35-qZBaHWmzlTi7J26L.0VN4IDOxwSO2EzNzEzW}`

- I typed `screen`
- This gave me the flag

## What I learned
- I learnt how to create virtual terminal using `screen`

## References 
Referred text given in challenge

---

# Detaching and Attaching
I was asked to first connect to the virtual terminal, then detach myself and atatch myself

## My solve
**Flag:** `pwn.college{0Dw3zhs86b2VUr15Tpius3Y6ciL.0lN4IDOxwSO2EzNzEzW}`

- I wrote `screen`
- Then I pressed `ctrl + d` followed by `a`
- Then I ran `/challenge/run`, and finally wrote `screen -r`
- This gave me the flag and I reattatched myself to the terminal

## What I learned
- I learnt how to deattatch and reattatch myself to virtual terminal using `screen`

## References 
Referred text given in challenge

---

# Finding Sessions
The challenge asks me to go through various screen sessions and find the flag

## My solve
**Flag:** `pwn.college{k5af6S30bQ5AXDCriGaL3k3fIN8.01N4IDOxwSO2EzNzEzW}`

- First found running sessions using `screen -ls`
- Then used `screen -r 147.session_a7563376053fa45a`
- This gave me the flag

## What I learned
- I learnt to check all running sessions using `screen -ls`
- Also learnt how to run a particular session using `screen -r`

## References 
Referred text given in challenge

---

# Switching Windows
I was asked to switch window from 1 to 0 using `ctrl + a`

## My solve
**Flag:** `pwn.college{sap_1RizS_Tg8Xw1HzuX-pBhbi0.0FO4IDOxwSO2EzNzEzW}`

- I typed `screeen -ls` to get all sessions
- Then went to deattatched session using `screen -r 135.challenge_session`
- Then simple changed to window 0 using `ctrl + a` then pressed `0`

## What I learned
- I learnt how to change windows using `ctrl + a` followed by a number from `0-9`
- We can even scroll using `ctrl + a` followed by `p` and `n` for previous and next
- `ctrl + a` followed by `"` brings up the selection menu

## References 
Referred text given in challenge

---

# Detaching and Attaching (tmux)
I was asked to use tmux to detach and reattach `tmux`

## My solve
**Flag:** `pwn.college{088Nv5BCBWDrJjhsWNU_1ZZoVUA.0VO4IDOxwSO2EzNzEzW}`

- I ran `tmux`
- Then pressed `ctrl + b` followed by `d` to detach it
- Ran `/challenge/run`
- Reattatched using `tmux a`

## What I learned
- I learn basics of `tmux`

## References 
Referred text given in challenge

---

# Switching Windows (tmux)
I was asked to switch to window 0 to get the flag

## My solve
**Flag:** `pwn.college{UWUqut7X950PWPQMN2PrQ87znhR.0FM5IDOxwSO2EzNzEzW}`

- I used `tmux`
- Then ran `ctrl + b` followed by `w`
- Then switched to window 0 and got the flag

## What I learned
- I learnt how to switch windows on tmux

## References 
Referred text given in challenge

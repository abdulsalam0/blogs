## OverTheWire: Bandit Level 0 -> Level 1

# Level 0 -> Level 1 Goal
The password for the next level is stored in a file called `readme` located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

Commands you may need to solve this level
ls, cd, cat, file, du, find

| Command | Explanation |
|---|-----------------------|
| ls | List directory contents |
| cd |change the working directory |
| cat | concatenate files and print on the standard output  |
| file | determine file type  |
| du | estimate file space usage |
| find | search for files in a directory hierarchy  |

### Key Parts

- Username: bandit0
- Remote address: bandit.labs.overthewire.org
- Port: 2220
- password: bandit0

### Solution:

This section is from the first article. This is the way you should ssh to a machine and make sure you remember the port flag.

The best way to show the content of the readme file is by using the `cat` command but before that, we can use the `ls` command to show the list of all the content inside this directory.

```
ssh bandit0@bandit.labs.overthewire.org -p 2220
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit0@bandit.labs.overthewire.org's password: bandit0

bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1

```

> Password: boJ9jbbUNNfktd78OOpsqOltutMc3MY1


### Conclusion
This challenge was about making you understand what the `ls` and `cat` commands do. Why you should use them and how they are used to show the password.

### Links to the challenge
- Bandit challenge: https://overthewire.org/wargames/bandit
- Level 0 -> 1: https://overthewire.org/wargames/bandit/bandit1.html
- Level 1 -> 2: https://overthewire.org/wargames/bandit/bandit2.html

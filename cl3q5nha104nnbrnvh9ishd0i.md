## OverTheWire: Bandit Level 0

# Level 0 Goal
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is `bandit.labs.overthewire.org`, on `port 2220`. The username is `bandit0` and the password is `bandit0`. Once logged in, go to the Level 1 page to find out how to beat Level 1.

### Learning Objectives
- SSH

### SSH

SSH or Secure Shell is a network communication protocol that enables two computers to communicate. If you are running Windows 10/11 you can run the ssh command from the cmd(command line). If you are running UNIX operating system you will be able to run the ssh command from the terminal.

### Key Parts

- Username: bandit0
- Remote address: bandit.labs.overthewire.org
- Port: 2220
- password: bandit0

### Solution:
```
 ssh bandit0@bandit.labs.overthewire.org -p 2220
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit0@bandit.labs.overthewire.org's password: bandit0
```

### Conclusion
This lesson was about getting you started with SSH and understanding the different parts of the command from the **username**, **remote address** and the **flags**. that way you are comfortable moving from one level to another level. 

### Links to the challenge
- Bandit challenge: https://overthewire.org/wargames/bandit/
- Level 0: https://overthewire.org/wargames/bandit/bandit0.html
- Level 0 -> 1: https://overthewire.org/wargames/bandit/bandit1.html
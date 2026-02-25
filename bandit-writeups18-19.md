level 18->19

Objective:The password for the next level is stored in a file readme in the home directory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

Initial Enumeration:
I tried to connect with SSH to the bandit18 user but i noticed that the moment i log in with the password it logs me out.

<img width="663" height="540" alt="kali-linux-2025 4-vmware-amd64-2026-02-25-10-22-16" src="https://github.com/user-attachments/assets/7a24ddb9-c7b9-42a8-abd5-4bc78a097912" />

Then i tried to see if commands worked after the ssh command like:
'ssh bandit18@bandit.overthewire.labs.org -p 2220 ls'
and i after i put the level's password it showed me the readme file.
So i did the same but now i use cat readme and i got the password for the next level.

Key concept learned:
That SSH allows remote execution of commands by adding them after the common SSH expression

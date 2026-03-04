Bandit Level 21->22

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

Initial Observation

I look in /etc/cron.d/ path and see that there are some files here.

<img width="1918" height="878" alt="kali-linux-2025 4-vmware-amd64-2026-03-04-10-25-48" src="https://github.com/user-attachments/assets/6e83d295-7666-435d-8010-31a14c7cc31a" />

Then i use the commmand:
cat cronjob_bandti22 to get info about what this cronjob does.

<img width="1918" height="878" alt="kali-linux-2025 4-vmware-amd64-2026-03-04-10-31-13" src="https://github.com/user-attachments/assets/a2956a6e-4fcc-4ab3-b76e-4524632c0621" />

This cronjob runs the /usr/bin/cronjob_bandit22.sh file as bandit22 user. The five start mean that it runs every minute, every day. Let's take a closer look to what is executed in this file now.
To do that i use the command:
cat /usr/bin/cronjob_bandit22.sh

Here is what we get!

<img width="1918" height="878" alt="kali-linux-2025 4-vmware-amd64-2026-03-04-10-38-35" src="https://github.com/user-attachments/assets/c745adc3-1ba2-46ef-978f-344070073764" />
This creates a file in the tmp folder and gives read permission to everyone. Then it copys the bandit22 password to that new file.

So to get the that password from the new file we just have to read the new file with the cat command.

BANDIT LEVEL 29->30

OBJECTIVE: Find the password stored in a Git repository where the main branch appears empty or redacted.

ENUMERATION:

After cloning the repository an ls command shows a README.md file stating that passwords are no longer stored in production. I checked the commit history using git log
but the password was not visible in the recent commits.

Then i realized there might be more branches besides the main branch.
Command: git branch -a

Observation: This reavealed some other branches as in the image below.

<img width="790" height="373" alt="kali-linux-2025 4-vmware-amd64-2026-03-25-15-02-18" src="https://github.com/user-attachments/assets/0a06312f-60b8-450c-8ed5-4b3744c5efeb" />

I switched to the other branches to check their contents:
Command: git checkout dev
Result: After switching branches, the README.md file contained the password for level 30.

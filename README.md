# My Linux Upskill Challenge Journal
BITA Kernel Crew · Cohort 1 · Sept 2026

## Day 0
- Set up my server (DigitalOcean / Killercoda) — it's alive 🐧
  - I am using a local Ubuntu server VM on my Proxmox server for this challenge
- Problems I hit and how I fixed them: none to list

## Day 1
- Problems I hit and how I fixed them:
  - 'ifconfig' command not found. Installed by running 'sudo apt install net-tools'.
  - 'ifstat' command not found. Installed by running 'sudo apt install ifstat'.
  - 'iftop' command not found. Installed by running 'sudo apt install iftop'.
   - After installation, I ran the 'sudo iftop -i enp1s0' command. Said hardware was not found. Did some research and was told that iftop is working but did not find the network interface because it doesn't exist. I was told to run 'ip link' to find the interface. Once I found it, I ran 'sudo iftop -i ens18'
 
## Day 2
- Problems I hit and how I fixed them:

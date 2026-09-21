# My Linux Upskill Challenge Journal
BITA Kernel Crew · Cohort 1 · Sept 2026 · See [Linux Upskill Challenge](https://linuxupskillchallenge.org/) and [Linux Upskill Challenge Playlist](https://youtube.com/playlist?list=PL4mta2djduQQaLFxhnJP1qw9y4IsJW-jU&si=bPrK8sx5ulsvU5r7)

## Day 0 -- COMPLETED
- Set up my server (DigitalOcean / Killercoda) — it's alive 🐧
  - I am using a local Ubuntu server VM on my Proxmox server for this challenge
- Problems I hit and how I fixed them: none to list

## Day 1 -- COMPLETED
- Problems I hit and how I fixed them: A few to report
  - 'ifconfig' command not found. Installed by running 'sudo apt install net-tools'.
  - 'ifstat' command not found. Installed by running 'sudo apt install ifstat'.
  - 'iftop' command not found. Installed by running 'sudo apt install iftop'.
   - After installation, I ran the 'sudo iftop -i enp1s0' command. Said hardware was not found. Did some research and was told that iftop is working but did not find the network interface because it doesn't exist. I was told to run 'ip link' to find the interface. Once I found it, I ran 'sudo iftop -i ens18'
 
## Day 2 -- COMPLETED w/ minor issues
- Problems I hit and how I fixed them: One to report
  - The TLDR command was not installed. I installed it with 'sudo apt install tldr'. The command still did not work after attempting to run 'tldr ls'. Ran updates on packages. Still did not work. Realized that I installed two different versions of the command; Python and Haskell. Removed Python version to see if that worked. It did not. So, I removed the Haskell version. Did some research and saw that there is a universal version called Tealdeer. Tried to install that but says that it cannot locate the package even after running updates. I will revisit this later. I will just have to use the 'man' command until then.

## Day 3 -- COMPLETED
- Problems I hit and how I fixed them: None to report
  - No problems, but I did create another user so that it can be strictly used for this challenge (I may have to go back and forth between the newly created user and my admin user).

## Day 4 -- COMPLETED
- Problems I hit and how I fixed them: None to report
  - Learned how to navigate using the "Midnight Commander" feature. Also, I learned how to launch a game of hangman.
 
## Day 5 -- COMPLETED
- Problems I hit and how I fixed them: None to report
  - Learned about tab completion, using the 'less' command, the 'more' command, and dot files.

## Day 6 -- 
- Problems I hit and how I fixed them:

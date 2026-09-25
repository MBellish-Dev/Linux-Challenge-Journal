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

## Day 6 -- COMPLETED
- Problems I hit and how I fixed them: No problems to report.
   - Learned how to navigate in VIM. Here are some shortcuts:
      - INSERT mode (by pressing "I" allows you to do just that.)
          - Hitting H, J, K, L will move the cursor left, down, up, and right respectively while in Insert mode.
      - Visual mode (by pressing "V")
          - Select a portion of text and use 'd' to delete.
          - Use "Y" to copy (yank), 'yy' to copy an entire line,'p' to paste, 'u' to undo, and CRTL + r to redo.
      - Normal mode (by pressing the Esc key)
          - x = delete/cut, dd = delete an entire line,
          - Use / -f to find and / -r to replace
      - Command mode (by pressing the colon [:] key)
          - This is where you can use the q - Quit, q! - force quit, W - save, wq - save and quit
 
## Day 7
- Problems I hit and how I fixed them:
  - Apache2 successfully installed. Will have to learn how to bring up the html page of my apache.
  - Ran 'curl -4 ifconfig.me' to find the public IP address. It would need to be accessed on a different network.

## Day 8
- Problems I hit and how I fixed them: None to report.
  - Using the "cat" command prints all the text/lines in file from top to bottom. Using "tac" (which is the reverse of "cat") prints from bottom to top.
  - Using the "grep" command pulls the text that you want to print (make sure the text you want to print is in parentheses) --> grep "example text" example.txt
    - grep -o means that you only want to see what you are searching. --> Will need to look at the grep command I copied from the video.
  - Using "uniq" will print the unique lines from the files
  - Using the "cut" command will only print based on the instructions you give it (i.e. cut -d"[insert what to cut]" -f[field number] [file name] -- with -d and -f being the limitators)
  - Learn more about "sed", "awk", and "RegEx" (regular expressions).

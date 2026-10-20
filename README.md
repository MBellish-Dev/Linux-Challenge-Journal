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
 
## Day 7 -- COMPLETED
- Problems I hit and how I fixed them: One to report
  - Apache2 successfully installed. Will have to learn how to bring up the html page of my apache.
  - Ran 'curl -4 ifconfig.me' to find the public IP address. It would need to be accessed on a different network.
  - Found the correct ip address to see the Apache web page.

## Day 8 -- COMPLETED
- Problems I hit and how I fixed them: None to report.
  - Using the "cat" command prints all the text/lines in file from top to bottom. Using "tac" (which is the reverse of "cat") prints from bottom to top.
  - Using the "grep" command pulls the text that you want to print (make sure the text you want to print is in parentheses) --> grep "example text" example.txt
    - grep -o means that you only want to see what you are searching. --> Will need to look at the grep command I copied from the video.
    - When running the grep command for "authenticating", but nothing was showing/printing. Maybe because of how my Ubuntu server VM is set up. *shrugs*
  - Using "uniq" will print the unique lines from the files
  - Using the "cut" command will only print based on the instructions you give it (i.e. cut -d"[insert what to cut]" -f[field number] [file name] -- with -d and -f being the limitators)
  - Learn more about "sed", "awk", and "RegEx" (regular expressions).

## Day 9 -- COMPLETED
- Problems I hit and how I fixed them: None to report
  - I already had 'ufw' installed and running on my server when I first created it almost over a year ago (sudo apt install ufw and sudo ufw enable and ssh with http).
  - I am still able to ssh it into my server using a terminal from a different PC on the same network.
  - Learned how to do port scanning with Nmap.
 
## Day 10 -- COMPLETED
- Problems I hit and how I fixed them: None to report
  - I have used the 'cron' command before when setting up an automated task for my Kali Linux virtual machine to scan my Windows 11 virtual machine.

## Day 11 -- COMPLETED
- Problems I hit and how I fixed them: None to report
  - Learned how to use the 'locate' command after installing it
  - Learned about updating the database using the 'sudo updatedb' command.
  - I can still use the grep command as well.

## Day 12 -- COMPLETED
- Problems I hit and how I fixed them: None to report.
  - This one was interesting to learn.
  - When using the 'sftp' method, you have to type out this command: 'sftp username@ipaddress'
    - Use the 'put' command (put "[drive name]\path\to\folder\and\file" -- this works with the local C: drive) to transfer files from local machine to the current directory of the Ubuntu server.
      - If you want a specific path, then follow up with the Ubuntu file path AFTER the file path of your local machine.
    - Use the 'get' command (get /home/path/to/folder/and/file "[drive name]\path\to\folder\and\file) to get files from Ubuntu server and send them to a location on the PC.
      - I believe that there is not default path for the receiving end. So, you HAVE to specify.
  - You can sync the two different folders by using 'rsync' (rsync -avh /windows/source username@ipaddress:/ubuntu/source/)
    - You can add 'dry-run' to test it out if not sure.
    - The flags -a, -v, and -h are options for the rsync
      - -a - archive mode -- preserves the things (copy/synchronize properly)
      - -v - verbose -- shows you what is happening with rsync (tell me what you are doing)
      - -h - human-readable -- makes things easy to read
  - Will use the 'rsync' command on a different machine

## Day 13 -- COMPLETED
- Problems I hit and how I fixed them: None to report
  - Learned how to create new users, create groups, add users to groups, and give them sudo privileges
  - Learned how to change the names of the users and the groups
 
## Day 14 -- COMPLETED
- Problems I hit and how I fixed them: None to report
  - Learned about changing the ownership of a file for users and groups.

## Day 15 -- COMPLETED
- Problems I hit and how I fixed them: None to report
  - When wanting/needing to install an additional package in a repository, should make sure that the private key is downloaded first so that when running 'apt' it will know that the package is coming from a legit source. This is also VERY beneficial to do as it provides a layer of security.
  - To add software not from official Ubuntu repositories, this is the command that you would run > sudo add-apt-repository ppa:<user>/<ppa-name>
  - This is how to remove the PPA:
    - sudo apt install ppa-purge
    - sudo ppa-purge ppa:<user>/<ppa-name>
  - APT > advanced package tool
  - DPKG > debian package

## Day 16 -- COMPLETED
- Problems I hit and how I fixed them: None to report
  - Learned how to zip and unzip files
  - Learned 'tarball' - single archive file created with 'tar' (usually compressed)
    - this is the command: tar cf archive.tar [file name #1] [file name #2] [file name #3] etc
      - C is for create. F is for file.
      - 'archive.tar' does not necessarily have to be that name
      - the total size of the tar file is the sum of the files being archived
    - this is the command to look inside the archive file: tar tvf [name of the archive file]
      - T is for table of contents, V is for verbose, and F is for file
    - this is the command to zip an archive file: tar czf compressed-archive.tar.gz [insert the names of the files that are in archive.tar]
      - C for create, Z for zip (compress), F for file
      - the file size will be smaller than the archive file
    - this is the command to extract the compressed archive file into another directory: tar xvf [name of the compressed archived tar] -C [directory location]
      - X for extract, V for verbose (to see it after it is done), and F for file
     
## Day 17 -- COMPLETED
- Problems I hit and how I fixed them: Minor issue with having an older version of nmap running
  - Learned what source code is
    - a human readable form for an application
  - Learned what binary is
    - it's for computers
    - the actual application
    - highly distributed on the repositories
  - "open source" and "free software" are pretty synonymous. "Open source" is a friendlier phrase.
  - When needing to get an older version of a source, instead of going to the website and downloading it, here is the command prompt method:
    - wget -v [insert link of source].tar.bz2 <-- the file may or may not be zipped
      - when extracting a bz2 zip file, this is what you start with: tar jxvf [insert name of bz2 file]
  - When installing a different version of Nmap (7.80 > 7.70), it still shows version 7.80 as the current version (instructional video shows version 7.70)
    - However, /usr/bin/nmap shows version 7.80, and /usr/local/bin/nmap shows version 7.70 (exactly like the instructional video)

## Day 18 -- COMPLETED
- Problems I hit and how I fixed them:
  - System Log -- historic record of system events
  - Logs themselves take up space over time. Use 'logrotate' to, well, rotate the logs. This helps to view the log at a point something took place, be better organized, and save disk space as well as the log itself.
    - Start with Log0. After a period of time has passed, it gets archived and a new log (Log1) is created. Then when time has passed, that log will get archived and another new log (Log3) will get created. Some can be archived for a very long time depending on the business or the policy that was set.
    - Link for reference: [Log Rotation](https://www.crowdstrike.com/en-us/cybersecurity-101/next-gen-siem/log-rotation/)
  - Daemon (pronounced "demon") - program/service that runs in the background
  - Journal - a way to check files, gather information, and do some filtering without having to dive into the log files themselves
    - Here are some commands:
      - journalctl -b < this shows what happened since the booting of the server
      - journalctl --since today < shows logs from the day
      - journalctl -f < shows logs as they are happening (used if you are trying to test something). '-f' is similar to 'tail' which shows the last (or recent) log.
      - journalctl --priority=[insert priority number]
        - 3 < shows only the error logs
        - 1 < shows what is critical
       
## Day 19 -- COMPLETED
- Problems I hit and how I fixed them:
  - shortcuts to files (go from this: /really/long/path/to/the/original/file to this: /home/shortcut --> file
  - Inode > index nodes - this describes a file system object and that it stores the attributes of that file (file permissions, file size, the user owner, the group owner) and it links those attributes to a block of data
  - Commands to run:
    - df -i > this shows you the amount of inodes a filesystem has
    - ls -i [insert file name] > shows the inode number of that particular file
    - stat [insert file name] > shows that status of a file including the inode number
  - Symlink (also known as soft link) and hard link. These help with shortcuts to a file
    - To create a softlink: ln -s [filename from] [filename to]
      - 'S' is for Symlink or softlink
    - You can use 'stat [insert file name #1] [insert file name #2]' to look at the status of both files and see that the file that has been symlink will say "symbolic link". The inodes are the same as well as the file size and permissions.
    - If original file of the softlink is deleted, then it will reference something that no longer exists
    - Use 'stat -L [insert file name #1] [insert file name #2]' to get a more in-depth look at the files.
  - Hard link - it references directly to the inode of the original file and goes to that data block.
    - Command(s) to use:
      - ln [filename from] [filename to] > this will create the hardlink
      - ls -li [filename from] [filename to] > this shows the same inode and file permissions
      - stat [filename from] [filename to] > shows more in-depth file information (same file size, inode, datablock, etc)
    - If original file of the hardlink is deleted, then
  - Alias - a shortcut for a command that is too long or used too often

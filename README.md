# Linux Cheat Sheet

Cheat sheet with most used linux commands

## Subtitle: 

Input             | Description
------------------|------------
**[ ]**           | Brackets only represent a user input (what you have to type)
**[file]**        | Type a file name + extension (".txt", ".css", ".js", etc)
**[folder]**      | Type a folder name
**[destination]** | Type a directory path
**[word]**        | Type a Word
**[host]**        | Type a remote computer name + IP adress (example: peterComputer@178.68.52.8)
**[PID]**         | Type a process ID. It's a number listed in "top" or "ps" command and identifies the process
**[site/IP]**     | Type a site name or IP adress


## Subtitle usage example: 

* Command description: ```touch [file]```
* Desired input #1: ```touch myFile.html```
* Desired input #2: ```touch hello.txt```

Below, the commands are organized in groups:

### Edit File 

Command                                 | Description 
----------------------------------------| -------------
nano **[file]**                         | Open file to edit
mv **[file]** **[file/destination]**    | Rename/move file
cp [file] **[destination]**             | Copy to destination
list -l                                 | List files with detailed info (l = long)
list -a                                 | List visible & insisible files (a = all)
rm -rf **[file]**                       | Remove (r = recursive, f = force)
rm * **[file]**                         | Wildcard. Removes all files with same letter combination or extension 

> Wildcard usage example:

rm *[file]  | Description
------------|-------------
rm *        | Remove all files
rm *.js     | Remove all javascript files
rm a*.txt   | Remove all text files beginning with letter "a"


### Find information in file 


Command                                 | Description 
----------------------------------------| -------------
cat **[file]**                          | Concatenate (print file content)
head **[file]**                         | Print file's fist 10 lines 
tail **[file]**                         | Print file's last 10 lines
less **[file]**                         | Print file with navigation
grep **[word]** **[file]**              | Search word and print line location
find -name **[file]**                   | Find file location

### Creating file/folder

Command                                 | Description 
----------------------------------------| -------------
touch **[file]**                        | Create file
mkdir **[folder]**                      | Create folder
echo **[word]** > **[file]**            | Write word inside file

### Info about commands

Command                                 | Description 
----------------------------------------| -------------
man **[command]**                       | Gets documentation about command
history **[command]**                   | Gets list of all typed commands
CTRL + R **[command]**                  | Reverse search. Find command from history, based on typed input
cd ~/.bash_history                      | Go to invisible file in HOME directory that contains command history

### SSH Key to remote computers 

Command                                 | Description 
----------------------------------------| -------------
ssh-keygen                              | Create SSH key pair
ls .ssh                                 | Confirm if SSH key was created
ssh-copy-id **[host]**                  | Copy SSH key to remote computer
ssh **[host]**                          | Login remote computer with SSH

### Network troubleshooting

Command                                 | Description 
----------------------------------------| -------------
ifconfig                                | Network info
hostname -I                             | IPV4 & IPV6 info
route                                   | If "default" line has IP, you can contact servers outside your local network
ping **[site/IP]**                      | Check "packet loss" summary to see if you get good internet connection
whois **[site/IP]**                     | Get all info about domain names registered in the internet
whois **[site/IP]** \| grep **[word]**  | Search for word inside whois command (\| = group commands together)
whois **[site/IP]** \| head             | Gets first 10 lines of whois command

### Process management 

Command                                 | Description 
----------------------------------------| -------------
top                                     | List processes executing in the computer
ps                                      | Similar to "ls" command but for processes
ps aux                                  | More detailed info
kill **[PID]**                          | Kill process

1. A world writable directory is more dangerous because it allows malicious threats to modify all
 the files inside of it such as replace or delete them.
 A world writable file only allows a threat to change the one file's contents.
 A directory such as uploads/ (777) allows a threat to put malicious scripts in and delete any files.
 This is very dangerous due to the fact that real systems can take control of them remotely

2. -perm -002 means that others have permission.
 The - stands for the bits set and its used to find writable files and who can modify the file.
 -perm /111 means any execute bit is set and the / means that any of those bits are set and its used to find
 executables. It determines whether the files can be ran or not.
 Different options are used to detect different problems. 
-002 detects unauthorized modification, /111 detects any execution that is not intended. 

3. If 50 world writable files are found then you should find which files are vulnerable.
 Then fix the permissions and remove the write access. Then check who owns the file.
 Then attempt to find where the files have been compromised and look for unauthorized changes.
 Then apply safety measures to make sure it does not happen again.

4. Find | while read runs a while loop in a child. This results in the count being updated in the child but once
 it exits it is lost therefore the count stays at 0. While read file; do runs it in the current shell and the count
 is able to update. | creates a child count while < <(...) keeps the count within the shell. 

5. I would use a cron table which is use for scheduling tasks to happen at a certain time.
 crontab -e implements the cron table then you would implement 0 2 * * * which means it runs at 2 am.
 I would also mail -s along with the email of the recipient to send it to the security team. 
 The line of code would look something like 
 0 2 * * * /home/student/cus1163-lab10/security_scanner.sh | mail -s "Report" recipientemail@gmail.com

Completeness score: 5 I feel that I completed everything that was asked
Comfortability Score: 4 It took a little getting used to but I was relatively comfortable
A win I had was being able to get the output to effectively show the 8 files. 

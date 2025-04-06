# Linux Practice - LAB02
## 1.List the available shells in your system.
```bash
cat /etc/shells
```
## 2.List all of the environment variables in your current shell.
```bash
set
compgen -v
```

## 3.Display your current shell name.
```bash
echo $SHELL
```

## 4.List all of the environment variables for the Bash shell.
```bash
set  
```

## 5.Edit your shell profile to display the date at login and change your prompt.
```bash
nano .bashrc
# write in this file 
echo "Welcome  today is $(date)"
```

## 6.Redirect the output of the ls command to a file called file_list.txt.
```bash
ls > file_list.txt
```

## 7.Use file globbing to list all .txt files in the current directory.
```bash
ls *.txt
```
## 8.Redirect the output of the ls command to a file and append it.
```bash
ls >> file_list2.txt
```
## 9.Use a pipe to send the output of ls to the grep command to filter for files containing the word "report".
```bash
ls | grep report
```

## 10.Use head to view the first 10 lines of a file, and tail to view the last 10 lines.
```bash
head file.txt
tail file.txt 
```
## 11.Use cut to extract the second column of a file called data.csv.
```bash 
cut -d , -f 2 data.csv
```

## 12.Search for all lines in a file called log.txt that contain the word "ERROR" using grep.
```bash
grep "ERROR" log.txt 
```

## 13.Create a shell variable called current_user to store the output of the whoami command.
```bash
current_user=$(whoami)
```

## 14.Use tr to convert a string of lowercase letters to uppercase.
```bash
echo "Momhamed Khaled" | tr [a-z] [A-Z]
```

## 15.Use a pipe to send the output of ps to grep to search for a specific process name.
```bash
ps | grep CMD
# CMD is a process
```
## 16.Create a Bash alias named ls for the command ls -l.
```bash
alias ls='ls -l'
```
## 17.Use sort to sort the output of ls -l by file size.
```bash
ls -l | sort -k5 -n
```
## 18.Use grep to count the number of lines that contain the word "success" in a file.
```bash
grep -c "success" file.txt
```
## 19.Redirect the output of the dmesg command to a file and view the first 20 lines using head.
```bash
dmesg > dmesg_output.txt
head -n 20 dmesg_output.txt
```
## 20.Use cut to extract the first field from a CSV file and display it.
```bash
cut -d , -f 1 file.csv
```
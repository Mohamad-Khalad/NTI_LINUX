
# Linux Practice - Bash Command Reference

## 1. Install Ubuntu [Dual-boot, VM, Multipass]
I used VM (Hyper-v)

## 2. What is the difference between `cat` and `more` command?
```bash
man cat
man more
```
```bash
cat displays the complete file, so if it is more than one screen full some of it scrolls out of view. 
more displays one screenfull at a time and you just tap the space_bar or enter to scroll up the next page.
```

## 3. What is the difference between `rm` and `rmdir` using man?
```bash
man rm
man rmdir
```
```bash
rm removes empty directories only.
rmdir removes files and directories.
```


## 4. Create the following hierarchy under your home directory:
```bash
mkdir dir1
mkdir dir1/dir11 dir1/dir12
touch dir1/dir11/file1
```

### a. Remove dir11 in one-step. What did you notice? And how did you overcome that?
```bash
rmdir dir1/dir11    # rmdir: failed to remove 'dir1/dir11': Directory not empty
rm -r dir1/dir11    # Overcome it by using rm -r reverse
```

### b. Then remove dir12 using `rmdir -p` command. State what happened to the hierarchy
```bash
rmdir -p dir1/dir12    # rmdir: failed to remove directory '/home/mohamed-kh': Permission denied
sudo rmdir -p dir1/dir12 # the hierarchy dir1 is removed
```

### c. The output of the command `pwd` was `/home/user`, write the absolute and relative path for `mycv`
```bash
/home/mohamed-kh/docs/mycv # Absolute path


./docs/mycv # Relative path 
```

## 5. Copy the `/etc/passwd` file to your home directory as `mypasswd`
```bash
cp /etc/passwd mypasswd
```

## 6. Rename this new file to be `oldpasswd`
```bash
mv mypasswd oldpasswd
```

## 7. You are in `/usr/bin`, list four ways to go to your home directory
```bash
cd
cd ~
cd $HOME
cd /home/moh-kh
cd -   
```

## 8. List Linux commands in `/usr/bin` that start with letter `w`
```bash
ls /usr/bin/w*
```

## 9. Display the first 4 lines of `/etc/passwd`
```bash
head -n 4 /etc/passwd
```

## 10. Display the last 7 lines of `/etc/passwd`
```bash
tail -n 7 /etc/passwd
```

## 11. Display the man pages of `passwd` the command and the file sequentially
```bash
man passwd && cat /etc/passwd # solution 1
man 1 passwd && man 5 passwd  # solution 2


```

## 12. Display the man page of the `passwd` file
```bash
man passwd # solution 1
man 5 passwd # solution 2
```

## 13. Display all commands that contain the keyword `passwd` in their man page
```bash
man -k passwd
```

## 14. Using `vi` write your CV in the file `mycv`
```bash
vi ./docs/mycv # open this file 
# (Then press 'i' to insert and write your CV: name, age, school, college, experience...)
# Press ESC
# :wq Save and exit with

```

## 15. Open `mycv` file using `vi` then:
```bash
vi ./docs/mycv
```

### a. Move the cursor down one line at a time
```bash
# Press 'j'
```

### b. Move the cursor up one line at a time
```bash
# Press 'k'
```

### c. Search for word `age`
```bash
# in normal mode Esc and write
/age
```

### d. Step to line 5
```bash
5G
```

### e. Delete the line you are on and line 5
```bash
dd    # deletes current line
5Gdd  # jumps to line 5 and delete it
```

### f. Step to the end of the line and change to writing mode in one step
```bash
A
```

## 16. List the available shells in your system
```bash
cat /etc/shells
```

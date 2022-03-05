# Popular Terminal Commands

## whoami

Type `whoami` to print the username currently logged in to the terminal session.

## man

Type `man <command>` to get the manual.

## clear

Type `clear` to clear all the previous commands that were ran in the current terminal. Shortcut: `Ctrl + L`.

## pwd

Call the `pwd` command to print the current working directory.

## ls

Type `ls` to list all the files that the directory contains. Use the `-a` or `--all` option to include all entries starting with `.`.

## cd

Type `cd <directory>` to change the working directory. Use the `..` special path to indicate the parent directory.

## mkdir

Type `mkdir <directory>` to make a directory. 

## touch

Type `touch <file>` to create an empty file. If the file already exists, it opens the file in write mode, and the file's timestamp is updated.

## rmdir

Type `rmdir <directory>` to remove a directory. The directory you remove must be empty.

## rm

To delete directories with files in them, use the `rm` command which deletes files and folders, using the `-r` option.

## open

Use `open` to open a file or a directory.

## mv

Use `mv` to rename or move files and directories.

```md
touch apple
mv apple new-apple
```

For example, the `apple` file is now moved to `new-apple`. This is how you rename files and folders.

If the last parameter is a directory, the specified files will be moved into that directory.

## cp

Use `cp` to copy a file.

```md
touch orange
cp orange new_orange
```

Use `-r` option to recursively copy the entire directory contents.

```md
mkdir fruits
cp -r fruits cars
```

## head

Use `head` to print the first 10 lines of the mentioned file to standard output.

## tail

Use `tail` to print the last 10 lines of the mentioned file to standard output.

## date

Type `date` to display the current time in the given format.

## > 

Use `>` to redirect the standard output to a file. The output will overwrite the file content if there's any.

```md
touch today.txt
date > today.txt
```

## >>

Use `>>` to append the standard output to a file.

## cat

`cat` is an abbreviation for concatenate. In its simplest usage, `cat` prints a file's content to the standard output.

```md
cat file1
```

Use `cat` to concatenate the content of multiple files into a new file.

```md
cat file1 file2 > file3
```

Use `-n` option to see the line numbers.

## less

Use `less` to show the content stored inside a file in a friendly interactive UI.

## echo

Use `echo` to print the output the argument passed to it.

```md
echo "Hello World"
```

Beware that special characters such as `$`, `*`, `~`, `?`, etc. They need to be escaped with a backslash `\`. 

## wc

Use `wc` to get useful information about a file or input received via pipes.

```md
wc -l test.txt // to count the lines
wc -w test.txt // to count the words
wc -c test.txt // to count the bytes
ls -al | wc    // to count the lines, words & bytes
```

## sort

Use `sort` to sort a text file contents or input received via pipes. `sort` has many options you can explore by calling `man sort`.

## uniq

`uniq` is a command that helps you sort lines of text. But, it will only detect adjacent duplicate lines. 

Use `uniq` along with `sort`:

```md
// to only display duplicate lines
sort test.txt | uniq -d 

// to only display non-duplicate lines
sort test.txt | uniq -u 

// to count the occurrences of each line
sort test.txt | uniq -c
```

## diff

Use `diff` to compare the differences between files or directories. 

There are many options you can explore in the man page by running `man diff`.

## find

Use `find` to find files or folders matching a particular search pattern. It searches recursively.

## grep

`grep` stands for global regular expression print. Use `grep` to search in files, or combine it with pipe to filter the output of another command.

## du

`du` stands for disk usage. Use `du` to calculate the size of a directory as a whole.

## df

Use `df` to get disk usage information.

## history

Type `history` to display all the history.

## ps

Use `ps` to monitor process status.

## top

Use `top` to display and update sorted information about processes.

## kill

Use `kill` to send a variety of signals to a program. Its main job is to terminate a program.

## killall

Similar to `kill`, `killall` send the signal to multiple processes at once instead of a sending a signal to a specific process id.

## jobs

When running a command in Linux / macOS, it can be set to run in the background using the `&` symbol after the command. For example: `top &`.

Use `jobs` to get the job number.

## fg

Use `fg` to resume the execution of commands in the foreground.

## bg

Use `bg` to resume the execution of commands in the background.

## gzip

Use `gzip` to compress a file using the gzip compression protocol named `LZ77`.

`gzip <file>` will compress the file, and append `.gz` extension to it. The original file is deleted. To prevent this, use `-c` option and use output redirection to write the output to the `file.gz` file.

```md
gzip -c file > file.gz
```

Or, use the `-k` option to keep the original file.

```md
gzip -k file
```

Use `-d` option to decompress a file.

```md
gzip -d file.gz
```

## gunzip

Use `gunzip` to decompress a file.

## tar

Use `tar` to create an archive, grouping multiple files in a single file.

`-c` option stands for create. `-f` option is used to write to file the archive.

```md
tar -cf archive.tar file1 file2
```

`-x` option stands for extract. `-C` option is used to extract them to a specific directory.

```md
tar -xf archive.tar -C directory
```

`-t` option to list the files contained in an archive.

```md
tar -tf archive.tar
```

`tar` is often used to create a compressed archive, gzipping the archive using `-z` option.

```md
tar -czf archive.tar.gz file1 file2
```

## nano

`nano` is a beginner friendly editor.

## alias

Use `alias` to create a new command.

```md
alias rm='rm -v'
```

The alias will work until the terminal session is closed. To make it permanent, add it to the shell configuration. This could be `~/.zshrc`, `/.bashrc` or `~/.profile` depending on the use case.

Be careful with quotes if you have variables in the command: if you use double quotes, the variable is resolved at definition time. If you use use single quotes, it's resolved at invocation time. Those 2 are different:

```md
alias lsthis="ls $PWD"
alias lscurrent='ls $PWD'
```

`$PWD` refers to the current folder the shell is in. If you now navigate away to a new folder, `lscurrent` lists the files in the new folder, whereas `lsthis` still lists the files in the folder where you were when you defined the alias.

## xargs

Use `xargs` to use the output of a command as the input of another command.

```md
command1 | xargs command2
```

## ln

Use `ln` to create links. Link is like a file that points to another file, similar to Windows shortcuts. They are 2 types of links: **hard links** and **soft links**.

## who

Use `who` to display the users logged in to the system.

## su

Use `su` to switch to a user account.

```md
su <username>
```

## sudo

`sudo` stands for super user do. Use it to run a command as root.

## passwd

Use `passwd` to change the password.

## chown

Use `chown` to change the file ownership from the owner (and the `root` user) to another user.

```md
chown <owner> <file>
```

Use `-R` flag to change the ownership of a directory, and recursively all the files contained, plus all the subdirectories and the files contained in them, too.

```md
chown -R <owner> <directory>
```

## chmod

Use `chmod` to change the permissions of a file or directory.

To use `chmod` to alter permissions, we need to tell it:
- **Who** we are changing permissions for?
- **What** change are we making? Adding? Removing?
- **Which** permissions are we setting?

The "**Who**":
- **u** - user (the owner of the file)
- **g** - group (members of the group the file belongs to)
- **o** - others (the "world")
- **a** - all of the above

The "**What**":
- \- (minus sign) removes the permission
- \+ (plus sign) grants the permission
- = (equals sign) set a permission and remove others

The "**Which**":
- **r** - the read permission
- **w** - the write permission
- **x** - the execute permission

For instance, add write permission to the group:

```md
chmod g+w file.txt
```


--- 

## File Attributes

The weird-looking 10 characters we see after sending `ls -l` are the file attributes.

The very first first character indicates the type of the file. Some of the more common types and their corresponding attributes are:

```md
- regular file
d directory
c character special file
l symbolic link
```

The remaining characters can be grouped into owner, group, and world. The first character of each group indicates the read permission, followed by the write permission and the execute permission.

| Types | Owner | Group | World |
| :---: | :---: | :---: | :---: |
| -     | rw-   | rw-   | rw-   |

Permissions:

| Character | Effect On Files | Effect On Directories |
| :---: | :--- | :--- |
| r | file can be read | directory's contents can be listed |
| w | file can be modified | directory's contents can be modified (create new files, rename files/folders) but only if the executable attribute is also set |
| x | file can be treated as a program to be executed | allows a directory to be entered or "cd"ed into |
| - | file cannot be read, modified, or executed depending on the location of the - character | directory contents cannot be shown, modified, or "cd"ed into depending on the location of the - character | 

---

For more info, please visit:
- [The Linux Command Handbook
](https://www.freecodecamp.org/news/the-linux-commands-handbook/#the-linux-man-command)
- [The 50 Most Popular Linux & Terminal Commands - Full Course for Beginners
](https://www.youtube.com/watch?v=ZtqBQ68cfJc&ab_channel=freeCodeCamp.org)

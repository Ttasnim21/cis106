# Question 1

## awk
* Description:
    * awk is a scripting language. awk works on programs that contain rules comprised of patterns and actions. The action is executed on the text that matches the pattern.
* Formula:
   * `awk + options + {awk command} + file`
   * `command output | awk + options + {awk command}`

* Examples:
    * How to print the first field of a file:
        * `awk -F':' '{print $1}' /etc/passwd`
    * How to start printing from a different line
        * `awk 'NR > 3 {print}' /etc/passwd`
    * How to change a field to upper case:
        * `awk -F: '{print toupper($1)}'`

## cat
* Description:
    * Used for seeing the content of a file. Also used for concatinating files.
* Syntax/Formula:
    * `cat + option + file or files to view/concatinate`
  
* Examples:
    * How to see the content of a file:
        * `cat /etc/passwd`
    * How to see the content of a file with line numbers:
        * `cat -n /etc/passwd`
    * How to see the content of a file with endling line character
        * `cat -E /etc/passwd`
        * Command Output:
```
gnome-initial-setup:x:125:65534::/run/gnome-initial-setup/:/bin/false$
hplip:x:126:7:HPLIP system user,,,:/run/hplip:/bin/false$
gdm:x:127:133:Gnome Display Manager:/var/lib/gdm3:/bin/false$
ttasnim:x:1000:100:ttasnim,,,:/home/ttasnim:/bin/bash$
vboxadd:x:999:1::/var/run/vboxadd:/bin/false$
fwupd-refresh:x:128:136:fwupd-refresh user,,,:/run/systemd:/usr/sbin/nologin$
_flatpak:x:129:138:Flatpak system-wide installation helper,,,:/nonexistent:/usr/sbin/nologin$
sshd:x:130:65534::/run/sshd:/usr/sbin/nologin$
```
## cp
* Description:
    * Used for copying files and directories to another location. To copy a file, specify “cp” followed by the name of a file to copy.
* Formula:
    * `cp + files to copy + destination` 
    * To copy directories: `cp -r + directory to copy + destination`
  
* Examples:
    * To copy a file:
        * `cp Downloads/wallpapers.zip Pictures/`
    * To copy a directory with absolute path:
        * `cp -r ~/Downloads/wallpapers ~/Pictures/`
    * To copy the content of a directory to another directory:
        * `cp Downloads/wallpapers/* ~/Pictures/` 
## cut
* Description:
    * The cut command is a command-line utility that allows you to cut out sections of a specified file or piped data and print the result to standard output. The command cuts parts of a line by field, delimiter, byte position, and character.
* Formula/Syntax:
    * The cut command takes the following syntax:
       `cut [option] [file]`

* Examples:
    * Cut by Bytes
    The -b option allows you to extract data using bytes. The syntax is:
       * `cut -b [LIST] [file]`
    * To extract the first byte from each input line, run:
       * `cut -b 1 employees.txt`
    * Cut by Characters
    To cut by characters, specify the -c option. Cutting by characters is similar to cutting by bytes, except you need to specify the character position rather than the byte position. The syntax is:
       * `cut -c [LIST] [file]`
    * The [LIST] argument specifies the characters to be extracted from each line of [file].
    For example:
       * `cut -c 10- employees.txt`
    * The output indicates that one user is currently logged in. Use the cut command to extract the logged-in user's username from the who command's output:
       * `who | cut -c 1-8`
    * Additionally, use cut to extract multiple different characters from a line. For example, display the username and login time of all logged-in users:
       * `who | cut -c 1-8,18-`
## grep
* Description:
    * Grep is an acronym that stands for Global Regular Expression Print.
    Grep is a Linux / Unix command-line tool used to search for a string of characters in a specified file. The text search pattern is called a regular expression. When it finds a match, it prints the line with the result. The grep command is handy when searching through large log files.
* Formula:
    * `grep [options] [pattern] [file]`
  
* Examples:
    * To Search a File
    To print any line from a file that contains a specific pattern of characters, in our case phoenix in the file sample2, run the command:
       * `grep phoenix sample2`
    * To Search Multiple Files
    To search multiple files with the grep command, insert the filenames you want to search, separated with a space character.
       * `grep phoenix sample sample2 sample3`
    * Search All Files in Directory
    To search all files in the current directory, use an asterisk instead of a filename at the end of a grep command.
       * `grep nix *`
    * To Find Whole Words Only
    Grep allows you to find and print the results for whole words only. To search for the word phoenix in all files in the current directory, append -w to the grep command.
       * `grep -w phoenix *`
## head
* Description:
    * The head command displays the top N number of lines of a given file. By default, it prints the first 10 lines. If more than one file name is provided then data from each file is preceded by its file name.
* Formula:
    * `head + option + file(s)`
  
* Examples:
    * Display the first 10 lines of a file
         * `head ~/Documents/Book/dracula.txt`
    * Display the first 5 lines of a file
         * `head -5 ~/Documents/Book/dracula.txt` 
## ls
* Description:
    *  The 'ls' command is used to list files and directories. The contents of your current working directory, which is just a technical way of stating the directory that your terminal is presently in, will be listed if you run the "ls" command without any further options.
* Formula:
    * `ls [options] [names]`

* Examples:
    * Long Listing of Files in Linux
        * `ls -l`
    * List Files with Human Readable Format
    With a combination of -lh option, shows sizes in a human-readable format.
       * `ls -lh`
    * List Files in Reverse Order in Linux
    The following command with the ls -r option display files and directories in reverse order.
       * `ls -r`
## man
* Description:
    * man command in Linux is used to display the user manual of any command that we can run on the terminal. It provides a detailed view of the command.
* Formula:
    * `man + command`

* Examples:
    * Executable programs or shell commands
        * `man ls` `man pwd`
    * System calls, which are system requests that programs make to the kernel
        * `man kill` `man read`
    * Library calls (to access functions in program libraries)
        * `man xcrypt` `man stdin` 
## mkdir
* Description:
    *  The mkdir command in Linux/Unix allows users to create or make new directories. mkdir stands for “make directory.” With mkdir , you can also set permissions, create multiple directories (folders) at once, and much more.
* Formula:
    * `mkdir + the name of the directory`

* Examples:
    * Create a directory in the present working directory
       * `mkdir wallpapers`
    * Create a directory in a different directory using relative path
       * `mkdir wallpapers/ocean`
    * Create a directory in a different directory using absolute path
       * `mkdir ~/wallpapers/forest`
## mv
* Description:
    * mv moves and renames directories
* Formula:
    * `mv + source + destination`
  
* Examples:
    * To move a file from a directory to another using relative path
        * `mv Downloads/homework.pdf Documents/`
    * To move a directory from one directory to another using absolute path
        * `sudo mv ~/Downloads/theme /usr/share/themes`
    * To move multiple directories/files to a different directory
        * `mv games/wallpapers/rockmusic/ /media/student/flashdrive/`
## tac
* Description:
    * The tac command is used for displaying the content of a file in reverse order. Just like cat, tac concatenates files and displays the output of the concatenation.
* Formula:
    * `tac + option + file(s) to display`
  
* Examples:
    * Display the content of a file located in the pwd
        * `tac todo.md`
    * Display the content of a file using absolute path
        * `tac ~/Documents/todo.md`
## tail
* Description:
    *  The tail command displays the last N number of lines of a given file. By default, it prints the last 10 lines. If more than one file name is provided then data from each file is preceded by its file name.
* Formula:
    * `tail + option + file`
  
* Examples:
    * Display the last 10 lines of a file
        * `tail ~/Documents/Book/dracula.txt`
    * Display the last 5 lines of a file
        * `tail-5 ~/Documents/Book/dracula.txt`
        * command output
```
sshd:x:130:65534::/run/sshd:/usr/sbin/nologin
```


## touch
* Description:
    * touch is used for creating files
* Formula:
    * `touch file_name`

* Examples:
    * To create several files
        * `touch list_of_cars_.txt script.py names.csv`
    * To create a file using absolute path
        * `touch ~/Downloads/games.txt`
    * To create a file using relative path
        * `touch Downloads/games2.txt` 
## tr
* Description: 
    * The tr command is a Linux command-line utility that translates or deletes characters from standard input ( stdin ) and writes the result to standard output ( stdout ). Use tr to perform different text transformations, including case conversion, squeezing or deleting characters, and basic text replacement.
* Formula:
    * `tr [OPTION] SET1 [SET2]`
  
* Examples:
  * A simple tr command use case is to change all lowercase letters in the text to uppercase and vice versa, as shown below.
```
$ cat linux.txt

linux is my life
linux has changed my life
linux is best and everthing to me..:)
```
```
$ cat linux.txt | tr [:lower:] [:upper:]

LINUX IS MY LIFE
LINUX HAS CHANGED MY LIFE
LINUX IS BEST AND EVERTHING TO ME..:)
```

  * Alternatively, you can use the following command to change all lowercase letters to uppercase in a file as shown.
```
$ cat linux.txt | tr [a-z] [A-Z]

LINUX IS MY LIFE
LINUX HAS CHANGED MY LIFE
LINUX IS BEST AND EVERTHING TO ME..:)
```
* To save the results written to stdout in a file for later processing, use the shell’s output redirection feature (>) as shown.

```
$ cat linux.txt | tr [a-z] [A-Z] >output.txt
$ cat output.txt 

LINUX IS MY LIFE
LINUX HAS CHANGED MY LIFE
LINUX IS BEST AND EVERTHING TO ME..:)
```

* In regards to the redirection, you can send input to tr using the input redirection and redirect the output to a file using the same command, as shown.

`$ tr [a-z] [A-Z] < linux.txt >output.txt`

## tree
* Description: 
    * The tree is a tiny, cross-platform command-line program used to recursively list or display the content of a directory in a tree-like format. It outputs the directory paths and files in each sub-directory and a summary of a total number of sub-directories and files.
* Formula:


* Examples: 
    * To list directory content in a tree-like format, navigate to the directory you want and run tree command without any options or arguments as follows. Remember to invoke sudo to run the tree in a directory that requires root user access permissions.
```
# tree
OR
$ sudo tree
```

   It will display the contents of the working directory recursively showing sub-directories and files, and a summary of the total number of sub-directories and files. You can enable the printing of hidden files using the -a flag.

   `$ sudo tree -a`

   * To list the directory contents with the full path prefix for each sub-directory and file, use the -f as shown.

   `$ sudo tree -f`

   * You can specify the maximum display depth of the directory tree using the -L option. For example, if you want a depth of 2, run the following command.

   `$ sudo tree -f -L 2`

   * There are also some useful file options supported by tree such as -p which prints the file type and permissions for each file in a similar way as the ls -l command.

   `$ sudo tree -f -p`

## vim
* Description: 
    *  Vim is a text editor that is an upgraded version of the Vi editor and is more compatible with Vi. The most usage of vi editors is to create a new file, edit an existing file, or just read a file. Vim editor is more useful in editing different kinds of plain text.
* Formula:
    * `vim [options] [filelist]`
  
* Examples:
    * To open a file using Vim you can use the following command (simply replace filename.css with your actual file name).

      * `vim filename.css`
    * According to Vim themselves, install Vim via Git is the simplest and most efficient method. Simply use the following commands:
    ```
     git clone https://github.com/vim/vim.git
     cd vim/src
     make
     ```
    * Install Vim on Ubuntu/Debian:
If you're using Ubuntu or Debian use apt-get to install Vim, like so:

       * `sudo apt-get install vim`

   * Install Vim on CentOS/Fedora:
If you're using CentOS or Fedora, use yum to install Vim:

      * `sudo yum install vim`
  
* Basic Vim commands:
     * :help [keyword] - Performs a search of help documentation for whatever keyword you enter

    * :e [file] - Opens a file, where [file] is the name of the file you want opened

    * :w - Saves the file you are working on

    * :w [filename] - Allows you to save your file with the name you've defined

    * :wq - Save your file and close Vim

    * :q! - Quit without first saving the file you were working on


## Question 2

  * How to work with multiple terminals open?
  
    Answer: open one terminal the open another terminal and set them side by side. Or user tillix and split the terminal as needed.

  * How to work with manual pages?
  
    Answer: To use man, you type man on the command line, followed by a space and a Linux command. man opens the Linux manual to the “man page” that describes that command—if it can find it, of course. We can type man man and see what man says about man. Then the man page for man opens. This is the man(1) page. Follow these tips to navigate the page:
      * To move through the man page one line at a time: Use the scroll wheel on your mouse, or the Up and Down arrow and Enter keys.
      * To move through the man page one screen at a time: Press the Space bar, and the PgDn and PgUp keys.
      * To move directly to the top or bottom of the man page: Press the Home and End keys.
    If you press H, you enter the help section and see a table of alternate keystrokes you can use. Those listed above will probably feel more natural to most people. To exit man, just press Q.

* How to redirect output (> and |) ?
  
    Answer: By default, stdout and stderr are printed to your terminal – that’s why you can see them at all. But we can redirect that output to a file using the > operator:
    ```
    $ echo hello
    hello
    $ echo hello > new-file
    $ cat new-file
    hello
    ```

    The second echo didn’t print anything to the terminal because we redirected its output to a file named new-file. Actually > new-file does two things:

    It creates a file named new-file if it doesn’t exist; and
    it replaces new-file’s contents with the new contents

    So if new-file already existed, and we did echo hello > new-file, it would now have only hello in it. If you want to append to the file, rather than replacing its contents, you can use the >> operator:
    ```
    $ cat new-file
    hello
    $ echo hello again >> new-file
    $ cat new-file
    hello
    hello again
    ```

    The | command is called a pipe. It is used to pipe, or transfer, the standard output from the command on its left into the standard input of the command on its right.

    # First, echo "Hello World" will send Hello World to the standard output.
    # Next, pipe | will transfer the standard output to the next command's standard input.
    # Finally, wc -w will count the number of words from its standard input, which is 2.
    echo "Hello World" | wc -w

* How to append the output of a command to a file?
  
    Answer: When the notation > > filename is added to the end of a command, the output of the command is appended to the specified file name, rather than writing over any existing data. The >> symbol is known as the append redirection operator.

* How to use wildcards (For copying and moving multiple files at the same time)
  
    Answer:  If you have a directory and want to copy multiple files, you can use the cp command. You need the names of the files and the destination directory. To select an entire folder, press Ctrl-A, and then click the first file and the last file. Shift-click the last file to select everything between them. Now, type the cp command to copy the files into another directory.

    To copy multiple files, highlight them with your mouse or keyboard. You can use a box to select all the files, or you can use the cp command. You can also use the xargs or GNU parallel command to copy files to several directories. After highlighting the files, you need to choose the destination directory. After you have selected the directory, you can use the cp command to copy the files.

    The cp command allows you to copy many files and directories at once. It is a useful tool for beginners, and comes with many options. In addition to copying multiple files, cp will also create a backup of any files that you may accidentally overwrite. To make sure your files don’t get overwritten, you can also specify the -i option. If you don’t specify the -i opYou can move multiple files in Linux by using the command line, a similar method to the one used on a modern user interface. The key is to hold down the Ctrl key while you click each file. Once you’ve selected several files, right-click them and drag them to a new location. There are a few different ways to do this. Below are some tips for desktop users. Read on to find out how to move multiple files in Linux.

    The mv command is used to move files between directories. It is very similar to the cp command, but allows you to move files physically. Unlike cp, the mv command will ask whether you want to overwrite existing files. Normally, you want to choose interactive mode and overwrite existing files. Force mode, on the other hand, overrides the interactive mode and can be dangerous.
* How to use brace expansion (For creating entire directory structures in a single command)
    
    Answer: Brace expansion {} is not a wildcard but another feature of bash that allows you to generate arbitrary strings to use with commands. For example,
    * To create an entire directory structure in a single command:
        * `mkdir -p music/{jazz,rock}/{mp3files,videoes,oggfiles}/new{1..3}`


# LINUX JOURNEY
## 1. The Shell

Quiz: What should be outputted to the display when you type echo Hello World?
A: Hello World

Exercises:
1. $ date = Wed Oct 16 09:27:13 UTC 2024
2. $ whoami = user

## 2. pwd (Print Working Directory)
Quiz: How do I find what directory you are currently in?
A: With the pwd command

## 3. cd (Change Directory)
Quiz: If you are in /home/pete/Pictures and wanted to go to /home/pete, what’s a good shortcut to use?
A: cd ..

Exercises: 
Run the cd command without any flags, where does it take you?
A: Takes you to your home directory. C:\Users\username

## 4. ls (List Directories)
Quiz: What command would you use to see hidden files?
A: ls -a

Exercises:
1. ls -R: This will display all files and directories recursively, starting from the current directory
2. ls -r: This will display files and directories in reverse order
3. ls -t: This will display files sorted by modification time, with the newest files listed first

## 5. touch
Quiz: How do you create a file called myfile?
A: touch myfile

Exercises:
1. Create a new file:
   touch testfile
2. Note the timestamp:
   ls -l
3. Touch the file and check the timestamp once again:
   touch testfile
   ls -l

## 6. file
Quiz: What command can you use to find the file type of a file?
A: Use the file command.

Exercises: 

$ file banana.jpg

Output:

banana.jpg [banana.jpg is identified as a JPEG image.]

$ file setup.exe

Output:

[This is an executable for example 64-bit file that is mostly used to install applications.]

## 7. cat
Quiz: What's a good way to see the contents of a file?
A: Use the cat command.

Exercises: 
Run cat on different files and directories. Then try to cat multiple files. 

§ cat testfile = (This file is empty, so there will be no output.)
$ cat testfile testfile2 = (This file is empty, so there will be no output.)

## 8. less
Quiz: How do you quit out of a less command?
A: With q

Exercises: 
Run less on a file, then page up and around the file. Try searching for a specific word. Quickly navigate to the beginning or the end of the file

Use the following command to navigate through less:

    q - Used to quit out of less and go back to your shell.
    Page up, Page down, Up and Down - Navigate using the arrow keys and page keys.
    g - Moves to beginning of the text file.
    G - Moves to the end of the text file.
    /search - You can search for specific text inside the text document. Prefacing the words you want to search with /
    h - If you need a little help about how to use less while you’re in less, use help.

## 9. history
Quiz: What is the command to clear the terminal? 
A: clear

Exercises:
Navigate through your previous command history with the Up and Down keys. Play around with ctrl-R reverse search:

$ history
Output:

1  date

2  whoami

3  pwd

4  cd /home

5  ls -l

...

## 10. cp (Copy)
Quiz: What flag do you need to specify to copy over a directory?

A: With r-

Exercises: Copy over a couple of files, be careful not to overwrite anything important.

A: $ cp mycoolfile /home/pete/Documents/cooldocs

Output:

(Copies `mycoolfile` to `/home/pete/Documents/cooldocs`)

## 11. mv (Move)
Quiz: How do you rename a file called cat to dog?

A: mv cat dog

Exercises: Rename a file, then move that file to a different directory.

A: mv testfile myfirstfile

## 12. mkdir (Make Directory)
Quiz: What command is use to make a directory?

A: mkdir

Exercises: Make a couple of directories and move some files into that directory.

A: 

$ mkdir documents images
Output:
(Creates `documents` and `images` directories)

$ mv file1.txt documents/
Output:
(Moves `file1.txt` into the `documents` directory)

$ mv photo.jpg images/
Output:
(Moves `photo.jpg` into the `images` directory)

## 13. rm (Remove)

Quiz: How do you remove a file called myfile? 

A: rm myfile

Exercises: 

1. Create a file called -file (don't forget the dash!).
2. Remove that file.

A: 

touch -file

rm file

## 14. find

Quiz: What option should I specify for find if I want to search by name? 

A: -name

Exercises: Find a file from the root directory that has the word net in it.

A: find / -name "*net*"

## 15. help

Quiz: How do you get quick command line help for built-in bash commands? 

A: help

Excercises: Run help on the echo command, logout command and pwd command

A: help echo

echo: echo [-neE] [arg ...]
    Write arguments to the standard output.
    
    Display the ARGs, separated by a single space character and followed by a
    newline, on the standard output.
    
    Options:
      -n	do not append a newline
      -e	enable interpretation of the following backslash escapes
      -E	explicitly suppress interpretation of backslash escapes
    
    `echo' interprets the following backslash-escaped characters:
      \a	alert (bell)
      \b	backspace
      \c	suppress further output
      \e	escape character
      \E	escape character
      \f	form feed
      \n	new line
      \r	carriage return
      \t	horizontal tab
      \v	vertical tab
      \\	backslash
      \0nnn	the character whose ASCII code is NNN (octal).  NNN can be
    		0 to 3 octal digits
      \xHH	the eight-bit character whose value is HH (hexadecimal).  HH
    		can be one or two hex digits
      \uHHHH	the Unicode character whose value is the hexadecimal value HHHH.
    		HHHH can be one to four hex digits.
      \UHHHHHHHH the Unicode character whose value is the hexadecimal value
    		HHHHHHHH. HHHHHHHH can be one to eight hex digits.
    
    Exit Status:
    Returns success unless a write error occurs.

  ## 16. man
  Quiz: How do you see the manuals for a command? 

  A: man

  Exercises: Run the man command on the ls command.

  ```bash
  LS(1)                            User Commands                           LS(1)

NAME
       ls - list directory contents

SYNOPSIS
       ls [OPTION]... [FILE]...

DESCRIPTION
       List  information  about  the FILEs (the current directory by default).
       Sort entries alphabetically if none of -cftuvSUX nor --sort  is  speci‐
       fied.
....
```
## 17. whatis
Quiz: What command can you use to see a small description of a command? 

A: whatis

Exercises: Run the whatis command on the less command.
 ```bash

less (1)             - opposite of more
less (3perl)         - perl pragma to request less of something

```

## 18. alias

Quiz: What command is used to make an alias? 

A: alias

Exercises: Create a couple of aliases then remove them.

A: 
alias list='ls -la'

unalias list

## 19. exit

Quiz: How can you exit from the shell? 

A: exit

Exercises: Exit out of the shell and see what happens. Make sure you don't need to do anymore work in that shell.
```
exit
bash: exit: shell: numeric argument required
Restarting Bash
```

# Advanced Linux Command Line

## Shell Interpreter Options
- shell interpreter handles commands from the terminal (or from a script)
- several have been developed, many have similar command support
- in 1979, Bourne shell was developed and one of the originals
- Bash (Bourne Again SHell) was created as a replacement or alternative for sh with features from ksh and csh

---

## Searching for files
> Locate files/directories with *find*
- Find files/directories below the current directory "." with a name *sampleDirectory*
```bash 
find . -name sampleDirectory
```

---

## Searching for content with *grep*
```bash 
grep -r "Linux is awesome" *
```

## Wildcard
- *\** means any files with any character in the name
- expanded by the shell to 
    ```
    grep -r "Linux is awesome" textfile.txt textfile1.txt textfile2.txt
    ```
- *textfile\*txt* means any textfile starting with *textfile* and ending with *txt*

## Pipes
- sends and output of one command to the input of another commmand
- chain commands together based on standard input/output
```bash
cat textfile1.txt | grep "Linux is awesome"
```

## Redirection
- send the output of a command to a new file using *>*
```bash
grep -r "Linux is awesome" * > searchResult.txt
```

- append the output of a command to an existing file using *>>*
```bash
echo "Linux is awesome" >> searchResult.txt
```

---

## File Permissions
- control how a file/directory may be used and by whom
- 3 levels of permissions - user, group, world(or everyone)
- execute permission typically not granted by default
- use chmod to change permissions
    ```bash
    chmod u+x helloworld.sh
    ```
- permissions can be specified by octal digits in numeric mode
    - 4 = read
    - 2 = write
    - 1 = execute
example:
```bash
chmod 766 helloworld.sh
```
---

## Remote Access
- you can use Secure SHell (ssh) for remote access to machines
```
ssh -p 2222 user@192.168.1.10
```
- use *scp* command for file transfer into/out of your machines
    - transfer from Windows to a virtual machine home directory
    ```bash
    scp -P 2222 /c/users/user1/Downloads/file.txt user@192.168.1.10:~
    ```
    
    - transfer from vm to a Windows system
    ```bash
    scp -P 2222 user@192.168.1.10:~/file.txt /c/users/user1/Downloads/file.txt
    ```


1. System Programming is similar to Application Programming in that both may interact with the kernel and C library.
        <form>
            <input type="radio" name="option" value="True" checked="true">True<br>
            <input type="radio" name="option" value="False">False<br>
        </form>
2. System programs can use system calls (syscalls) to invoke kernel functions from user space.
        <form>
            <input type="radio" name="option" value="True" checked="true">True<br>
            <input type="radio" name="option" value="False">False<br>
        </form>
3. As an alternative to using system calls to invoke kernel functions, user space applications can be directly linked with kernel space functions.
        <form>
            <input type="radio" name="option" value="True">True<br>
            <input type="radio" name="option" value="False" checked="true">False<br>
        </form>
4. Select examples of wrapper functions provided by the C library glibc (select any which apply)
    - [x] System calls
    - [x] Threading support
    - [ ] Compilation
5. APIs ensure source compatibility.  This means: 
        <form>
            <input type="radio" name="option" value="True">Application executable files can be copied from one hardware platform to another and will be expected to run successfully on the new platform.<br>
            <input type="radio" name="option" value="False" checked="true">Application source code can be compiled for another platform and expected to work properly.<br>
        </form>
6. Select all the true statements about ABIs (select any which apply):
    - [x] Can define how an application interacts with itself
    - [x] Can define how an application interacts with libraries
    - [x] Can define how an application interacts with the kernel
    - [ ] Enforced by the toolchain for a platform
    - [ ] Defines interfaces by which one piece of software communicates with another at the source level
7. In Linux, most everything is accessed as a file, except for device access, which is handled completely differently.
        <form>
            <input type="radio" name="option" value="True">True<br>
            <input type="radio" name="option" value="False" checked="true">False<br>
        </form>
8. A Linux file's inode contains the following parameters (select any which apply):
    - [ ] Filename
    - [x] Modification timestamp
    - [x] Owner of the file
    - [x] Location of the file's data on disk
9. Linux Directories are used to map names with which to access files.
        <form>
            <input type="radio" name="option" value="True" checked="true">True<br>
            <input type="radio" name="option" value="False">False<br>
        </form>
10. Select the types of Linux files referred to as "Special files" (select any which apply):
    - [x] Block devices
    - [x] Character devices
    - [x] Named pipes
    - [ ] Directories
    - [ ] Links
11. Block devices and character devices are similar in that they can both address memory on byte boundaries as opposed to sector boundaries.
        <form>
            <input type="radio" name="option" value="True">True<br>
            <input type="radio" name="option" value="False" checked="true">False<br>
        </form>
12. Block devices and character devices are similar in that they are both considered "Special files".
        <form>
            <input type="radio" name="option" value="True" checked="true">True<br>
            <input type="radio" name="option" value="False">False<br>
        </form>
13. Processes use memory virtualization, meaning each process appears to use its own single linear address space.
        <form>
            <input type="radio" name="option" value="True" checked="true">True<br>
            <input type="radio" name="option" value="False">False<br>
        </form>
14. Two threads running under the same Process each use their own process memory space and can't access each other's memory.
        <form>
            <input type="radio" name="option" value="True">True<br>
            <input type="radio" name="option" value="False" checked="true">False<br>
        </form>
15. The uid value of 1 is associated with a special user known as root.
        <form>
            <input type="radio" name="option" value="True">True<br>
            <input type="radio" name="option" value="False" checked="true">False<br>
        </form>
16. Select the permission represented by the octal value 755:
        <form>
            <input type="radio" name="option" value="True" checked="true">Owner may read, write execute. Group and Everyone else may read and execute only<br>
            <input type="radio" name="option" value="False">Owner may read, write, execute. Group and Everyone else may read and write only<br>
        </form>
17. Select the permissions represented by the octal value 640:
        <form>
            <input type="radio" name="option" value="True" checked="true">Owner may read and write only. Group may read only. Everyone else has no access<br>
            <input type="radio" name="option" value="False">Owner may read and write only. Group may write only. Everyone else has no access<br>
            <input type="radio" name="option" value="False">Owner may read, write and execute. Group may write only. Everyone else has no access<br>
        </form>
18. Signals are used as a one-way asynchronous notification mechanism for a process.
        <form>
            <input type="radio" name="option" value="True" checked="true">True<br>
            <input type="radio" name="option" value="False">False<br>
        </form>
19. The Ctrl-C handler is an example of what type of communication mechanism in Linux?
        <form>
            <input type="radio" name="option" value="True" checked="true">Signal<br>
            <input type="radio" name="option" value="False">Interproces Communication<br>
        </form>
20. Which of the following is an Absolute Pathname  
        <form>
            <input type="radio" name="option" value="True">home/user/Documents<br>
            <input type="radio" name="option" value="True">httpd/httpd.conf<br>
            <input type="radio" name="option" value="True">usr/bin/env<br>
            <input type="radio" name="option" value="False" checked="true">/etc/httpd/httpd.conf<br>
        </form>
21. Which of the following is a Relative Pathname
        <form>
            <input type="radio" name="option" value="True">/etc/httpd/httpd.conf<br>
            <input type="radio" name="option" value="True" checked="true">httpd/httpd.conf<br>
            <input type="radio" name="option" value="True">/home/user/Documents<br>
            <input type="radio" name="option" value="False">/usr/bin/env<br>
        </form>



    





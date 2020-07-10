---
title: "Linux, A Brief History"
teaching: 0
exercises: 0
questions:
- "How does Linux come to be?"
objectives:
- "Understand the history behind the development of UNIX and later Linux"
keypoints:
- "Linux comes out of the effort of researchers in industry and academic to develop a better interface 
  between computers and human."
---

**The Dawn of Computing: System Operators**
- First commercial computer by IBM: IBM 701 (1952)
  - Require system operators to help run the programs
- Second generation: IBM 704 (1956)
  - Incompatible with IBM 701
  - No support from IBM
  - No textbook/documentation
- IBM 704 system operators
  - Trained by IBM for 701
  - Encouraged by IBM to organize informal meetings to share expertise

**From single-purpose to time-sharing**
- Concept of time-sharing: Operating System
- Allows computers to become generali-purposes (serving multiple users running different programs)
- Enables system operators to transition into the role of system administrators
- MIT, General Electric (GE), and Bell Labs collaborate to create the first time-sharing system call Multics
Multiplexed Information and Computing Service

**The birth of UNIX**
- Bell Labs left Multics in 1964 (over budget, behind schedule)
- Ken Thompson, Rudd Canaday, Dennis Ritchie continued working on Multics 
- Summer 1969
  - Ken Thompson’s wife and kids were out of town for a month
  - One week was assigned for each key components of UNIX (the operating system, the shell, the editor, and the assembler).

**UNIX**
- UNiplexed Information and Computing Service
- An emasculated Multics
- By 1971: as, cal, cat, chdir, chmod, chown, cmp, cp, date, dc, du, ed …
- By 1973: 16 new UNIX installations (components)
- C programming language (Dennis Ritchie)
- Pipe (designed by Doug McIlroy, implemented by Ken Thompson)

**A new era for UNIX**
- Ritchie, D.M. and Thompson, K., 1973. The UNIX time-sharing system. ACM SIGOPS Operating Systems Review, 7(4), p.27.
- After 6 months, number of UNIX installation tripled. 
- Due to AT&T’s antitrust settlement in 1958, UNIX cannot be sold as a product, but Bell Labs still retains licensing right
- Individual software and licenses must be shipped to others.
- 1974: Berkeley UNIX (BSD - Berkeley Software Distribution - led by Robert Fabrey at University of California at Berkeley)
- 1976: V6 (John Lions at University of New South Wales - Australia)
- 1982: SunOS (Sun Microsystem by Bill Joy - graduate student of Robert Fabrey)
- 1983: AT&T UNIX System V (after court-ordered divestiture of AT&T in 1983)

**The rise of Skywalker system administrators**
- Managing general-purpose computing systems requires a different set of skills.
- Serving a wide variety of users and applications.
- Universities were early leaders in fostering system admin groups (Purdue, Utah, Colorado-Boulder, and SUNY Buffalo were the initial hotbeds).
- Evi Nemeth: Mother of system administration
  - Graduate student administrative team.
- A system administrator
  - Jack of all trades
  - Rabid jacks of all trades: Hardware, software, system configuration, programming …
- 1989: First edition of UNIX and Linux System Administration Handbook

**The birth of Linux**
- Late 1990, UNIX was gaining ground everywhere …
- 1992: AT&T filed copyright lawsuit against BDSI and the Regents of University of California
- 1994: The lawsuit was settled and three files were removed from BSD code base.
- Impact was lasting
  - Everyone moved to Microsoft Windows
- 1984: Andrew Tennenbaum of Vrije Universiteit in Amsterdam developed MINIX as a learning software for his students.
- 1992: Linus Torvalds, an undergraduate at University of Helsinki, Finland, developed his own OS called Linux, with inspirations from both UNIX and MINIX.
  - UNIX administration skill sets applies directly to Linux

**Linux Announcement**
- Post Dot-com Bubble Burst
- Unix and Linux becomes more mainstream, as their TCO for computing servers was significantly lower than that of a Windows server. 
- It is not a war, but rather the right combination of Windows and Unix/Linux systems within an organization. 
- With its new CEO, Windows is embracing Linux and open-source
  - [Link to article discussing the new Windows subsystem for Linux](https://www.anandtech.com/show/14301/microsoft-build-day-1-windows-subsystem-for-linux-gets-more-linux)
  - [Link describe Windows' new command line tool](https://www.theverge.com/2019/5/6/18527870/microsoft-windows-terminal-command-line-tool)

**Where will Unix/Linux be in the future?**
- Cloud
- IoT (small devices)

**The Linux Filesystem**
- Everything in Linux is a file
- The Linux filesystem is used to store all information relevant to the long-term state of the system, including:
  - operating system kernel,
  - executable files for commands supported by the OS,
  - configuration information,
  - temporary work files,
  - user data,
  - special files that give controlled access to system hardware and OS functions.

**The Linux Filesystem**
- Start up and login to your Linux environment (depending on your courses, this could be a virtual machine or a remote Linux environment).
- At the terminal, type the following commands (hit the Enter key after each command).
- The `$` sign represents the prompt at the terminal. you do not retype `$`.
- Run the following commands:

### Hands-on
 Run the following commands
> ~~~
> $ cd / 
> $ clear 
> $ ls -ls -d */
> ~~~ 


{: .bash}
> ~~~
> The Linux Filesystem (Ubuntu)
> /: The root directory
> /dev: Hardware devices
> /bin: Essential low-level system utilities
> /usr:
> /usr/bin: Higher-level system utilities and application programs
> /usr/lib: Program libraries for high-level user programs
> /lib: Program libraries for low-level system utilities
> /sbin: Superuser system utilities (for system administrative tasks)
> /tmp: Temporary file storage space (can be used by any user)
> /home: User home directories containing personal directory for each user
> /etc: Configuration and information files (for system and user programs )
> /proc: A pseudo-filesystem to be used as an interface to the Linux kernel. It includes a sub-directory for each running process (run ls /proc and then ps aux to see the process ID matches up with the subdirectories)
> ~~~
{: .output}

The Linux Filesystem (Ubuntu)
/root: The personal directory space of the root user
/snap: The directory for Ubuntu's package management utility
/lost+found: abandoned files recovered by fsck but could not be placed into an exact location will be placed into this directory.
/lib64: Program libraries (similar to /lib) for 64-bit only programs.
/media: Contains mount points for removable media
/srv: Data for services provided by the system
/opt: Add-on application software packages 
/sys: Virtual directory for system information
/run: Run-time variable data
/boot: Static files of the boot loader
/mnt: Mount point for mounting a file system temporarily
/var: Variable data

**The Linux Filesystem (Ubuntu)**
- Path: In a file system, a path allows a user/program to access a final location (file or directory) within that file system by following the hierarchical structure of directories leading to that location.
- Relative Path: A path starting from your current location.
- Absolute Path: A path starting from the root directory (/)


**Where are you in a Linux Filesystem?**
- `pwd`: system command to print the full (absolute) path of the current working directory
- When login as a normal user, you typically start at `/home/<your_user_name>`
- As you move around the Linux Filesystem, pwd lets you know the path from `/` to where you currently are.


What else are there in a Linux Filesystem?
ls: list directories
Full documentation: http://man7.org/linux/man-pages/man1/ls.1.html
ls alone prints out the content of the current directory
ls with a path to a directory prints out the content of that directory
Additional flags (-l, -a, ...) can be used with ls to provide more information
You can run man ls to view more information about the command inside the terminal.


How do you get from here to there?
cd: change directory
Run the following commands in your Linux terminal


cd without target will change to home directory
cd with .. with move up one directory level
$ pwd
$ cd /tmp
$ pwd
$ cd
$ pwd


Other commands to manage the Linux Filesystem
mkdir: make directory
rmdir: remove directory
cp: copy
mv: rename or move files/directories
rm: remove the specified files or directories

Viewing files (ASCII/text-based files)
cat: catenate - displays the contents of the target file(s) on the screen.
more: cat with scroll-by-page views (forward only).
less: more with the ability to scroll backward. 

References
https://www.levenez.com/unix/
Nemeth, E., Snyder, G., Mouat, A., Branca, F., Hein, T.R., Whaley, B., Mackin, D. and Garnett, J., 2018. UNIX and Linux system administration handbook.

{% include links.md %}


An operating system (OS) is a piece of system software that handles computer hardware and software resources while also providing common services to computer programmes.

Time-sharing operating systems schedule operations to make the machine more effective. They can also provide accounting tools for expense distribution of processing time, mass storage, printing, and other services.

Since the application code is normally run directly by the hardware and often makes device calls to an OS function or is interrupted by it, the operating system serves as an interface between programmes and the computer hardware for hardware functions such as input and output and memory allocation. Operating systems can be used on a variety of computer-containing machines, ranging from cellular phones to laptop computers.
Operating systems can be used on a wide range of computer-based products, from cellular phones and video game consoles to web servers and supercomputers.

While the majority of the operating systems mentioned above have a respectable graphical user interface, it is critical to recognize and leverage the Command Line Tool's ability. The command-line tool, also known as Linux Shell, provides access to new functions that are not accessible in the graphical user interface (GUI). On the command line, which is referred to as the command prompt, you will still type after the $ symbol.

### What is Linux? 
Linux is an operating system that is built on the UNIX operating system (Mac OS is based on UNIX OS as well). Linus Torvalds developed Linux, which is distributed as free and open-source software. There are many Linux distributions, also known as "distros." Among them are:

1. Debian
2. Ubuntu
3. Fedora
4. RedHat Enterprise Linux (RHEL)
5. Arch Linux
6. Chrome OS

Commercial distributions include RHEL and Chrome OS. About 90% of the world's servers run a Linux-based distribution. It is secure, free, and fast.
You docker is mostly in the Linux based kernels and web-engine are Linux thus everything is Linux.

Linux is technically is not a very fitted definition to the OS but they are well-built kernels. Thus we build operating system on top of this kernel, Thus any OS let it be Ubuntu,Debian,Arch or any flavor is developed on the Linux kernel.

Thus kernel is the one that interfaces with our Hardware i.e. CPU,RAM,Memeory etc., when we want run a `application` OS that we have installed will communicate with the file system and get the packages and will fire-up the application and allocate the hardware or the resource to run the application.

## Why linux?
Linux is a open-source distribution,they are faster and are more secure.
They are also:
* High stability

The Linux operating system is very stable and does not crash often. And after many years, the Linux operating system still operates as quickly as it did when it was first installed. Most of us have probably seen how a newly installed Windows device runs incredibly quickly and then becomes sluggish after six months to a year. Then, much of the time, the only choice is to reinstall the operating system and all other software.
And also they are compatible with the Embeded operating system,they can also be run on edge.

* Customizable

The Linux operating system is very stable and does not crash often. And after many years, the Linux operating system still operates as quickly as it did when it was first installed. Most of us have probably seen how a newly installed Windows device runs incredibly quickly and then becomes sluggish after six months to a year. Then, much of the time, the only choice is to reinstall the operating system and all other software.

The majority of prominent browsers have Linux versions. The Linux theory is focused around the use of multiple small programmes, each of which performs a single mission exceptionally well. These programmes, though, can be merged to create extremely efficient programmes and utilities. The Linux operating system has a command line gui and many shells to select from.

System managers may take advantage of the efficient command line interface to write shell scripts to automate routine maintenance and other activities.

Embedded operating systems are computing systems that are programmed to run on embedded hardware. They are intended to run on small machines with limited autonomy (e.g. PDAs). They are designed to be very lightweight and highly powerful, and they can run with a small amount of capital. Examples of embedded operating systems include Windows CE and Minix-3

To open your terminal the keyboard short cut is `ctrl+T` on your keyboard where you will be able to open the terminal.

#### We use the Commad prompt for the linux commands

For some times get rid of your "GUI" mindset and try these commands. All these commands are the file system in the linux kernel thus you all will get an 

`pwd` Linux Command

Print Working Directory :just prints the directory which you have The name of the actual working directory is printed by pwd. When you launch a terminal, you are in the home directory of the person who has signed in. The utter direction is printed by pwdprint. It begins with a /, which is the source, or foundation, of the Linux File System.


`cd` Linux command

This command's is to modify the directory. To put it another way, it allows you to swap between file lists. For example, if you wanted to move from the home directory to the myfile directory, you would type:

`cd /myfile/application`
Also, note that . represents the current directory and .. represents the parent directory.
```
# takes you to your home directory (comment)
cd 
# To navigate to the parent directory
cd ../
# To change to previous working directory
cd ~
```

`ls` command

In the Linux world, the **ls** command is the most basic and widely used. The ls command, also known as the list command, displays all of the important files or directories specified within a certain file system in the Linux terminal. For example, consider the command:

`ls /<folder_mame>`

`man` command

One of the strongest Linux commands is the **man** command. The manual order is another name for this command. It's used to show the manual use of the inserted instruction. In other words, it is Linux's meta-command. Entering the man command displays all of the command's detail. As an example:

`man ls` : The above command will display all the necessary information about the ls command.

`man sudo_root` : This gives good information about the root directory.


`cat` command

The **cat** Linux command is an abbreviation for **concatenate**. It displays file information in the Linux terminal window. This is much more efficient than opening the file in an editor. Enter the following command to read the data from the. Bash log out file:

`cat .bash_logout`

`mkdir` command

**mkdir** Linux is a fundamental command in the Linux world. This instruction, as the name implies, is used to create a directory or, in other words, it is used to create a directory. The command below will generate a new folder called a test folder.

An example of the mkdir command:

`mkdir testfolder`

`chmod` command

The **chmod** command is used to change the permissions or flags of a folder or file. The flags specify who can read and write to a file or folder. One of the most important commands in the Linux world. Administrators make extensive use of it.

For example,

`chmod -R 7 test.txt`

`rmdir` command

**rmdir**, like the mkdir Linux command, is a commonly used command. Users may use this command to delete any file or directory from a specific location. To put it another way, you can use this order to uninstall a certain directory. The following instruction, for example, would delete the mydirectory from the system.

`rmdir mydirectory`

`touch` command

The **touch** command is similar to the **mkdir** command. The key distinction between touch and mkdir is that touch requires users to generate a text file or a.doc file.

For example

`touch mytestfile.txt`

`locate` command

`locate` command is another name for the locate button. This command is used to search or find a certain file. This command is one of the most commonly used in Linux. This command is very handy if you don't know the precise name of the file or the exact location of the file. The following command will look for a file that contains the words "result," "final," and "total."

For Example:

`locate -i *result*final**total*`

`clear` command

This instruction, as the name implies, is used to clear the Linux window terminal. To use this command, simply type clear and then press enter. In the Linux command line environment, this is the most commonly used command.

Command: `clear`

`rm` command

Just like _rmdir_ which removes the directory, **rm** command is used to remove the particular file. Suppose you want to remove .txt file or a .doc file then rm command is useful.

For example: `rm mytestfile.txt`

`cp linux command`

Copy files from location1 to location2. Directories can be copied using the `-R` option.
```
# copy file from your home to directory to another location
cp test.txt /tmp/bckup 
# copy contents of directories recursively
cp -R test_dir /tmp/bckup
```

`mv` command

**mv** command is one of the most commonly found in a Linux environment. This command allows the user to transfer a file to a certain directory. 

For example : `mv/myfolder/appli/myapps /myfolder/newapp/firstapp`

```
# Renaming file a.txt to b.txt
mv a.txt b.txt
# move file from directory test in your current directory to tmp
mv test/test.txt /tmp/test.txt
# move multiple files in your current directory to /tmp
mv a.txt b.txt c.txt /tmp 
# move file from a dir A to dir B by specifying the absolute paths
mv /var/log/test.log /tmp/test.log
```

`del` command is used for deletign the directory that we dont want to use.

14. curl command
**Curl** is used to retrieve data from Uniform Resource Locators (URLs) or IP addresses. If it is not already available in your Linux environment, you must first use the apt-get command to instal the curl programme.

Command : `curl https://github.com/torvalds/linux`

`echo` command

The __echo__ command prints the required text on the terminal pane. For example, if you want to print the text "Hello World" on the terminal window.

you can use this command : `echo Hello World`

`free` command

The __free__ command is used to produce memory consumption statistics. It computes the internal Random Access Memory (RAM) as well as the swap memory.

For example : `free -h`

`groups` command

One of the most critical commands in Linux environments is `groups`. This command specifies a certain user's membership. In other words, it indicates the consumer belongs to which party. 

For example:

`groups scott`

`groups thomas`

`head` command

The __head__ command displays the first ten lines of a given file. If you want to read fewer characters, use the -n suffix.

For example : `head -myfile.c`

`history` command

The __history__ command is one of the most commonly used and relevant Linux commands. This command returns a list of previously used commands. You just need to enter history to use this instruction.

Just type `history` in cmd.

`passwd` command

One of the useful Linux commands is the _password_ key, which is used to modify your own password. The administrator also uses this instruction to modify the passwords of other users as well.

For example : `sudo passwd jeff`

`ping` command

The __ping__ command is the most commonly used command in the Linux world. This command is often used to test the network link or troubleshoot networking problems. To use this command all you have to do is provide an IP address after ping. For example

Example : `ping <IP address>/<web URL>`

`alias`

The __alias__ command instructs the shell to replace one string with another when executing the commands. When users often need to execute a single instruction several times, they use a technique known as an alias. Alias is similar to an alternate command that does the same functions as if they were answering the entire command.

Example : `alias rm='rm -i'`

The above alias will stop unintentional deletion.

`ZIP`

__ZIP__ is a Linux file compression and packing service. Each file is stored in its own.zip file with the extension. nada. Zip is a file box tool that is used to shrink files in order to reduce file space. Zip is available for free in a variety of operating systems, including Unix, Linux, and Windows. The software is useful for packaging a series of files for sharing, archiving files, and creating backups,as well as for preserving storage space by temporarily removing extra files or folders

Example : `zip newfile.zip name.txt`

`dd`

__dd__ is a command-line utility for Linux operating systems that changes and copies files. This is one of the most crucial instructions. dd can also be used to perform tasks like backing up the boot region and obtaining a thickened mass of temporary files. It can also execute transformations on the data as it is represented, such as byte order exchange and conversion to and from ASCII and EBCDIC.

Example `dd if = /dev/hda of = ~/hdadisk.img`

The command above is used to generate a hard disc file. The dd command can also be used to backup a CDROM and restore a hard disc file.

`chown`

Users may use the __chown__ command to change the user and/or community control of a certain file, directory, or representative connection. Both files in Linux are associated with an owner and a collection, and they are distributed with access preferences for the file owner, segments, and others. In Linux, each user is associated with a set of characteristics. These features include a user ID and a directory. Users may connect more users to a unit or a group to simplify the process of managing users. In this case, a specified user may be linked to a "default category." It may even be a section of another category on the machine. Standard users of Linux can only change the group of a file if they have file rights and only to the group of which they are a branch. Modifications may be made when managing users.

Example : `sudo chown root myfile1.txt`

`sudo`

The __sudo__ command allows users to run programmes as a separate user, by default the root. If the user spends a lot of time at the prompt, sudo is one of the commands that they would use most. This is the most crucial order. In Linux, sudo stands for “Super User DO.” It is usually used as a prefix to any instruction that only the superuser is allowed to execute.When someone prefixes a Linux command with “sudo,” the command runs with heightened privileges, or in other words, provides a user with specific authorizations to execute a command as superuser.

Example : `sudo apt-get update`

`tail`

Displays the last part of files. By default, if the file is passed, it prints the last 10 lines

`tail -f /var/log/syslog`

`hostname`

print/set the hostname of the machine. Only the superuser can update the hostname
```
# print hostname of system
hostname
# set hostname 
hostname set name <host_name>.
```

`lsblk`

lsblk(Expanded as list block devices) is used for listing out all the block devices in a tree-like fashion. It also provides information about the partitions that are present on the block device.

`uname`

Print system information. There are multiple options that can be passed if you want a piece of specific information about the system like kernel-version, processor type, hardware-platform e.t.c.,
```# Prints all the information about the system
uname -a```

`df`

This commands reports file system disk space usage.
```# lists all the file system, use -a option in human readable format i.e., power of 1024
df -ah```

`du`

Estimates file space usage. It has various options to display the output in the format you desire.
```
# Display disk usage of all files and directories in the current directory
du -ah
# sum of sizes of files and directories in the directory specified
du -sh /home/test_user
```

`grep`

This command prints all the lines in a file that match a specific pattern.
```
# recursively grep for a pattern in a directory tree
grep -r search_field /etc/
# search two different words
egrep -w 'x|y' /home/test_user/*
```


`find`

This command searches a folder hierarchy to find a file or a directory that matches the specified name or pattern. It does a recursive search in all the directories down the tree.

```
# find a file with name test.txt in a folder
find /home/test_user -name test.txt
# find file of specific pattern recursively 
find . -type f -name "*.sh" -R
# find and remove multiple files following a same pattern
find . -type f -name "*.py" -exec rm -f {}
```

After all the struggle, you would be saying, man, this guy is still kicking himself for his decision (of using linux). No, not at all, because the machine is mine. I gain the freedom to do whatever I want about it while still getting a comfortable production setup that I can bring with me everywhere I go. The possibilities for having an atmosphere that makes me happier to use every day are simply linked to my desire to learn more about a topic.

The possibilities for creating an experience that I enjoy using on a daily basis are simply linked to my need to learn more about this kernel or the operating system.

I'll keep experimenting and tinkering; this machine will be with me for years to come, and this adventure has only just begun.

I hope you enjoyed this post; if you did, please leave a message or tell me about your own experience. Stay tuned for the other articles also.
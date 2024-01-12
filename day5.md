# Advanced Linux User!
## Some advanced user commands:
- to change password of user,type: sudo passwd username
- to change user id,type: sudo usermod -u new_id username
- to delete user: sudo userdel -r username
- to change users: u - username 
## sudoers file:
- The sudoers file is a file Linux and Unix administrators use to allocate system rights to system users
- The user you created doesn’t have power to use sudo as the original one.
- This is Because it is not Added in the sudoers file
- To access this file: sudo visudo
- You can add the User you need to have access to the sudoers file, so he can use the sudo command
## Linux File permission:
- every file on linux have their own owner and permissions.
- there are 5 main parts on the  listing: permission,owners,date,size,filename
#### Ownership:
- Ownership is the owner of the file
- This have two kinds:user and group
- to change the owner of the file, type:" chown user:group filname"
#### Permission:
- there are 3 types of permissions: read(r),Write(w),Execute(x)
- The folders and files are differ with the ‘d’ and ‘-’ on the beginning of  the permission.
- The permissions have 3 parts: user-group-other
- user(u)=> power of user defined on the the ownership
- Group (g )=> power of group defined on the the ownership
- Other ( o ) => power of other users.
- All ( a ) => power of all which can be found in the 3 above owners
- Command to change permission of file: chmod option filename
--->example: chmod +x day5.md (giving the permission for day5 to be executed)
##### CHMOD command:
- This command helps to change file permission.
- Those file permissions are read,write & execute.
-  Each of the permission have a number representations
--->Read -> 4 - r
--->Write -> 2 - w
--->Execute -> 1 - x
- syntax: chmod parameter filename
- the parameter can be in numbers and symbols
A) parameters in symbol:
- chmod a+x filename -> adding execute permission for all ( chmod +x filename)
- chmod u+x filename -> adding execute permission for user
- chmod g+x filename -> adding execute permission for group
- chmod o+x filename -> adding execute permission for other
- chmod -x filename -> removing execute permission for all
- chmod a+rwx , u-rw , g-x , o-xw filename -> gives rwx for all and removes something from all
B) parameters in number:
- chmod 621 filename -> 6 for user, 2 for group, 1 for other ( 6 = 4+2 ),6 =r w
- chmod 777 filename -> 7 for users, 7 for group , 7 for others (7 =4+2+1), 7 = rwx.
### Special File Permissions:
- There are another 3 special permissions, you may encounter on your pentest journey
- They are:
->SUID bits(s) - set user ID bit - add 4 infront of our numeric value ->4000
-> SGID bits(S) - set group ID bit - add 2 infront of our numeric value ->        2777
-> Sticky bits(t) - set other ID bit - add 1 in front of our numeric value -> 1602
- They are permissions like the execute(x), but they will set the execute permission to the user who settled them.
- Example: if mr.A add suid bit to a program that program will be executed with permission of mr.A
--->Meaning if admin add suid bit on some program. Then any user if they got that program they can run it as root with any sudo password
### Package installation on Linux:
-  ON linux to install softwares you use package managers.
-  Ex: apt,pacman,pkg,...
- We will use debian package manager.
- On debian the package manager i called APT’ also there is called‘dpkg’
- Package managers are a free-software user interface that work with an online server to handle the installation and removal of software on Debian, and Debian-based Linux distributions.
### Advanced package tool /apt/:
-  Apt is a free-software user interface that work with an online server to handle the installation and removal of software on Debian, and Debian-based Linux distributions.used for online and offline purpose
- the old 'apt' used as 'apt-get'
- syntax:
-->sudo apt update
--> sudo apt search <softwarename>
--> sudo apt install <softwarename>
--> sudo apt remove <softwarename>
--> sudo apt upgrade
--> sudo apt purge <sofwarename>
### Package Dependencies:
- A software can be built based on another program called ‘modules’
- SO, a program to work properly, the dependencies have to be installed successfully.
- Those package managers install the software+dependencies.
#### DpKg /Debian package manager/:
- Dpkg is an offline package managing program.
- Packages on debian have an extension “.deb”
- Syntax:
-->sudo dpkg -i <packagename>
-->sudo dpkg -r <packagename>
-->sudo dpkg -P <packagename>

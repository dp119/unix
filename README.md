
# <h2> Unix Commands for day-to-day activities #


# <h3> Command to copy directory or a filename from one machine to another. Below command works on the source machine

	
	scp -r directory|filename username@machine:targetpath

	scp -r logs chkuat02@chkuatap009:~/





# <h3> Command to find the disk space (in GB)

	
	df -h




Command to list the directories and their size

	
	df -h --max -depth=1



# <h3> Command to find filename or directory

	
	find . -type d -aname logs

	find . -type f -name test.log



# <h3> Command to send file attachment via mail and without any body

	
	mailx -s subject -a attachment dp@gmail.com < /dev/null



# <h3> Command to find the unix version 

	
	cat /etc/*release

# <h3> Command to find RAM usage, CPU usage

	
	free -m
	
	sar -r
	

	
# <h2> To find the list of all open files in unix

	lsof
	

# <h3> List of open files by a specific user

	lsof -u dprasad
	
	
# <h3> Find processes using specific port or Find if a port is listening

	lsof -i TCP:22
	netstat -aon
	
# <h3> List Only IPv4 & IPv6 Open Files

	lsof -i 4
	lsof -i 6
	
# <h3> List open files of TCP port ranges 1-1024

	lsof -i TCP:1-1024
	
# <h3> Exclude User with ‘^’ Character

	lsof -i -u^root #excludes root user in this example
	

# <h3> Find Out who’s Looking What Files and Commands

	lsof -i -u dprasad

# <h3> Search by PID

	lsof -p 100
	
# <h3> Kill all activity of particular user

	kill -9 `lsof -t -u dprasad`
	

# <h3> What is the difference between UNIX and LINUX?

	Unix originally began as a propriety operating system from Bell Labs and spawned into different commercial versions
	
	Linux is a OS based on UNIX, it is free and open source intended as non-proprietary OS


# <h3> Difference between df and duplicate


	du == Disk Usage. It walks through directory tree and counts the sum size of all files therein. It may not output exact information due to the possibility of unreadable files, hardlinks in directory tree, etc. It will show information about the specific directory requested. Think, "How much disk space is being used by these files?"

	df == Disk Free. Looks at disk used blocks directly in filesystem metadata. Because of this it returns much faster that du but can only show info about the entire disk/partition. Think, "How much free disk space do I have?"


# <h3> How to install any package in linux

	yum install


# <h3> What are ip tables in linux?

IP tables command line interface used to setup and maintain netfilter firewall for IPv4 included in linux kernel.

The firewall matches packets rules defined in these tables and takes specified action.
	
	RULE is the condition used to match packet
	CHAIN is the Collection of rules
	TABLE is Set of Chain
	TARGET is the action to be taken when a possible rule matches. It can be ACCEPT DROP or QUEUE
	POLICY is the default action taken in case of no match. It can be accept or drop.
	
	Configuration is saved in the file 				/etc/sysconfig/system-config-firewall
	After clicking Apply this file is overwritten 	/etc/sysconfig/iptables 


# <h3> How to install Tomcat package in LINUX (steps)

For private IP address
	
	ifconfig -a
	hostname -I | awk '{print $1}'
	
	
For public IP address
	
	curl ifconfig.me
	

Below are the files to configure IP address

	vi /etc/sysconfig/network
	vi /etc/resolv.conf
	

# <h3> How to check ip address in linux and where to set the ip address config?


# <h3> Check running processes 

	ps -ef 
	
# <h3> Check if a service is running

List all services in init system
	
	service [service_name] status
	service --status-all | more
	service --status-all | grep running
	service httpd status
	service httpd start
	service httpd stop
	
	
List all services in systemd system
	
	systemctl
	systemctl status apache2
	systemctl | grep apache2
	systemctl | grep running
	systemctl list-units --type service
	
	
	
	pstree 			# this gives output from SysVinit system
	chkservice		# new tool but needs super user access
	


# <h3>  Default for FTP, HTTP, HTTPS

	FTP 21
	HTTP 80
	HTTPS 443
	SSH 22


# <h3> How to change file permissions and ownership

	chmod +x filename
	chmod -w filename
	
	+ adds
	- removes
	= set permissions
	
	Eg:
	$chmod o+wx,u-x,g = rx testfile							# o is other, u is user, g is the group
	$ls -l testfile
	-rw-r-x-wx  1 dp119   users 1024  Nov 5 00:11  testfile
	
	
	chown user filename
	
	chgrp group filelist 		# to change the group
	

# <h3> How to change file permissions to files in specific directory in specific extensions

	chmod -R 755			# permissions to all files and subfolders in the tree 
	
	find /opt/lampp/htdocs -type d -exec chmod 755 {} \; 			# to change permissions only to directories recursively
	
	find /opt/lampp/htdocs -type f -exec chmod 644 {} \;			# to change permissions only to files recursively



# <h3> Difference between more and less commands in Linux


# <h3> Unix concepts to be refreshed


	Inode

	In unix filesystem, in all directores, find all unique files using hashmap function (not to use filename or size or timestamp) in python and remove all duplicate files

	netstat

	vmstat

	Unix script to read a file line by line and pass it as a parameter to another command

	git stash

	difference between branch and tag in git

	What are heira files in puppet

	how to merge changes from forked repo to original repo

	Ways of authenticating in Jenkins and job level authorization

	List of python libraries used
	
	Print the number 104 in words - "one hundred and four"
	
	Uses of /etc folder

# <h6> *This is a markdown file. Learn more about it [here](https://guides.github.com/features/mastering-markdown/) .*

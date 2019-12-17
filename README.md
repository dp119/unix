
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
	

# <h6> List of open files by a specific user

	lsof -u dprasad
	
	
# <h6> Processes using specific port 

	lsof -i TCP:22
	netstat -aon
	
# <h6> List Only IPv4 & IPv6 Open Files

	lsof -i 4
	lsof -i 6
	
# <h6> List open files of TCP port ranges 1-1024

	lsof -i TCP:1-1024
	
# <h6> Exclude User with ‘^’ Character

	lsof -i -u^root #excludes root user in this example
	

# <h6> Find Out who’s Looking What Files and Commands

	lsof -i -u dprasad

# <h6> Search by PID

	lsof -p 100
	
# <h6> Kill all activity of particular user

	kill -9 `lsof -t -u dprasad`
	

# <h4> Unix concepts to be refreshed


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

# <h6> *This is a markdown file. Learn more about it [here](https://guides.github.com/features/mastering-markdown/) .*

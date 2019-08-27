
# <h2> Unix Commands for day-to-day activities #


# <h3> Command to copy directory or a filename from one machine to another. Below command works on the source machine

	*
	scp -r directory|filename username@machine:targetpath

	scp -r logs chkuat02@chkuatap009:~/





# <h3> Command to find the disk space (in GB)

	*
	df -h




Command to list the directories and their size

	*
	df -h --max -depth=1



# <h3> Command to find filename or directory

	*
	find . -type d -aname logs

	find . -type f -name test.log



# <h3> Command to send file attachment via mail and without any body

	*
	mailx -s subject -a attachment dp@gmail.com < /dev/null



# <h3> Command to find the unix version 

	*
	cat /etc/*release

# <h3> Command to find RAM usage, CPU usage

	*
	free -m
	
	sar -r
	

# <h6> *This is a markdown file. Create one yourself from [here](https://guides.github.com/features/mastering-markdown/) .*

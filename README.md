
# <h1> Useful Unix Commands for day-to-day activities #


# <h3> Command to copy directory or a filename from one machine to another. Below command works on the source machine #

scp -r directory|filename username@machine:targetpath

scp -r logs chkuat02@chkuatap009:~/





# <h3> Command to find the disk space (in GB) #

df -h




# <h3> Command to list the directories and their size#

df -h --max -depth=1



# <h3> Command to find filename or directory#

find . -type d -aname logs

find . -type f -name test.log

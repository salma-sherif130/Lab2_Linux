# Lab2_Linux
#note : i cleared the output by mistake so i couldn't attach it.


#List the available shells in your system

    cat /etc/shells

#List all of the environment variables in your current shell.

    env
    
#Display your current shell name.

     echo "$SHELL"
     
#List all of the environment variables for the Bash shell.

    env
    
#Edit your shell profile to display the date at login and change your prompt.

    sudo nano ~/.bashrc 
    echo "Today is $(date)" 

#Redirect the output of the ls command to a file called file_list.txt.

    ls ~/.bashrc > file_list.txt
    
#Use file globbing to list all .txt files in the current directory.

    ls *.txt

#Redirect the output of the ls command to a file and append it.

    ls >> file_list.txt

#Use a pipe to send the output of ls to the grep command to filter for files containing the word "report".

    ls | grep report

#Use head to view the first 10 lines of a file, and tail to view the last 10 lines.

    head /etc/passwd
    tail /etc/passwd

#Use cut to extract the second column of a file called data.csv.

    cut -d',' -f2 data.csv

#Search for all lines in a file called log.txt that contain the word "ERROR" using grep.

    grep "ERROR" log.txt

#Create a shell variable called current_user to store the output of the whoami command.

    current_user=$(whoami)

#Use tr to convert a string of lowercase letters to uppercase.

    echo "salma" | tr 'a-z' 'A-Z'

#Use a pipe to send the output of ps to grep to search for a specific process name.

    ps -e | grep tty

#Create a Bash alias named ls for the command ls -l.

    vi ~/.bashrc
    alias ls='ls -l'

#Use sort to sort the output of ls -l by file size.

    ls -l | sort -k5 -n

#Use grep to count the number of lines that contain the word "success" in a file.

    grep -c "success" file_list.txt

#Redirect the output of the dmesg command to a file and view the first 20 lines using head.

    dmesg > new
    head -20 new

#Use cut to extract the first field from a CSV file and display it.

    cut -d',' -f1 data.csv

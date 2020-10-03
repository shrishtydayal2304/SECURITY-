TOUCH command Optional Reading Material
touch command in Linux with Examples
The touch command is a standard command used in UNIX/Linux operating system which is used to create, change and modify timestamps of a file. Basically, there are two different commands to create a file in the Linux system which is as follows:

cat command: It is used to create the file with content.

touch command: It is used to create a file without any content. The file created using touch command is empty. This command can be used when the user doesn’t have data to store at the time of file creation.

Using touch Command
Initially, we are in home directory and this can be checked using the pwd command. Checking the existing files using command ls and then long listing command(ll) is used to gather more details about existing files. As you can see in the below figure there is no existing files.

Click to enlarge

Touch command Syntax to create a new file: You can create a single file at a time using touch command.

Syntax:




touch file_name
The file which is created can be viewed by ls command and to get more details about the file you can use long listing command ll or ls -l command . Here file with name ‘File1‘ is created using touch command.

Click to enlarge

Touch command to create multiple files: Touch command can be used to create the multiple numbers of files at the same time. These files would be empty while creation.

Syntax:

touch File1_name File2_name File3_name 
Multiple files with name Doc1, Doc2, Doc3 are created at the same time using touch command here.

Click to enlarge

touch Command Options
Like all other command Touch command have various options. These options are very useful for various purpose.

touch -a: This command is used to change access time only. To change or update the last access or modification times of a file touch -a command is used.




Syntax:

touch -a fileName
Here touch -a command changes access time of the file named Doc1.

Click to enlarge

touch -c : This command is used to check whether a file is created or not. If not created then don’t create it. This command avoids creating files.

Syntax:

touch -c fileName
Click to enlarge

touch -c-d : This is used to update access and modification time.

Syntax:

touch -c-d fileName
Click to enlarge

touch -m : This is used to change the modification time only. It only updates last modification time.




Syntax:

touch -m fileName
Click to enlarge

touch -r : This command is used to use the timestamp of another file. Here Doc2 file is updated with the time stamp of File 1.

Syntax:

touch -r second_file_name first_file_name
Click to enlarge

touch -t : This is used to create a file using a specified time.

Syntax:

touch -t YYMMDDHHMM fileName
Fullscreen
Default view
20. LS command Optional Reading Material
22. NANO Command Optional Reading Material

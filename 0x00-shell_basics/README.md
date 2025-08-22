# This readme file for first assignment
Author: Khaled Mahmoud
Year: 2025

|Project | summary | command|
|--------|---------|--------|
|0-current_working_directory|Write a script that prints the absolute path name of the current working directory.|`pwd`|
|1-listit|Display the contents list of your current directory.|`ls`|
|2-bring_me_home|Write a script that changes the working directory to the user’s home directory. You are not allowed to use any shell variables|`cd ~`|
|3-listfiles|Display current directory contents in a long format|`ls -l`|
|4-listmorefiles|Display current directory contents, including hidden files (starting with .). Use the long format.|`ls -la`|
|5-listfilesdigitonly|Display current directory contents.Long format.with user and group IDs displayed numerically.And hidden files (starting with .)|`ls -lan`|
|6-firstdirectory|Create a script that creates a directory named my_first_directory in the /tmp/ directory.|`mkdir /tmp/my_first_directory`|
|7-movethatfile|Move the file betty from /tmp/ to /tmp/my_first_directory.|`mv /tmp/betty /tmp/my_first_directory`|
|8-firstdelete|Delete the file betty.The file betty is in /tmp/my_first_directory|`rm /tmp/my_first_directory/betty`|
|9-firstdirdeletion|Delete the directory my_first_directory that is in the /tmp directory|`rm -r /tmp/my_first_directory`|
|10-back|Write a script that changes the working directory to the previous one|`cd -`|
|11-lists|Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the /boot directory (in this order), in long format|`ls -al . .. /boot/`|
|12-file_type|Write a script that prints the type of the file named iamafile. The file iamafile will be in the /tmp directory when we will run your script|`file /tmp/iamafile`|
|13-symbolic_link|Create a symbolic link to /bin/ls, named `__ls__`. The symbolic link should be created in the current working directory|`ln -s /bin/ls $PWD/__ls__`|
|14-copy_html|Create a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.You can consider that all HTML files have the extension .html|`cp --update *.html ..`|
|100-lets_move|Create a script that moves all files beginning with an uppercase letter to the directory /tmp/u.You can assume that the directory /tmp/u will exist when we will run your script|`find . -name '[A-Z]*' -print0 | xargs -0 mv -t /tmp/u/`|
|101-clean_emacs|Create a script that deletes all files in the current working directory that end with the character ~|`find . -name '*~' -print0 | xargs -0 rm -f --`|
|102-tree|Create a script that creates the directories welcome/, welcome/to/ and welcome/to/school in the current directory.You are only allowed to use two spaces (and lines) in your script, not more|`mkdir -p welcome/to/school`|
|103-commas|Write a command that lists all the files and directories of the current directory, separated by commas (,).Directory names should end with a slash (/). Files and directories starting with a dot (.) should be listed. The listing should be alpha ordered, except for the directories . and .. which should be listed at the very beginning. Only digits and letters are used to sort; Digits should come first. You can assume that all the files we will test with will have at least one letter or one digit. The listing should end with a new line|`ls -amp`|
|school.mgc|Create a magic file school.mgc that can be used with the command file to detect School data files. School data files always contain the string SCHOOL at offset 0.|`file -C -m school.magic `|

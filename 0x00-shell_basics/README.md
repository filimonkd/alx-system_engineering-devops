# Description for each script



1. 0-current_working_directory

   * Script that prints the absolute path name of the current working directory

2. 1-listit

   * Script that display the contents list of your current directory.

3. 2-bring_me_home

   * script that changes the working directory to the user’s home directory.

4. 3-listfiles

   * Script that display current directory contents in a long format.

5. 4-listmorefiles

   * Script that Display current directory contents, including hidden files (starting with .). Use the long format.

6. 5-listfilesdigitonly

   * Script that display current directory contents with user and group IDs displayed numerically in long format including hidden files

7. 6-firstdirectory

   * Script that create my_first_directory directory in /tmp directory

8. 7-movethatfile

   * Script that describe how to move file

9. 8-firstdelete

   * Script that deletes betty file in /tmp/my_first_directory directory

10. 9-firstdirdeletion

    * Script that deletes my_first_directory directory in /tmp directory

11. 10-back

    * Script that returns the working directory to previous one

12. 11-lists

    * Script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the /boot directory (in this order), in long format.

13. 12-file_type

    *Script that prints the type of the file named iamafile

14. 13-symbolic_link

    * Script that creates a symbolic link to /bin/ls, named __ls__

15. 14-copy_html

    * Script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.

16. 100-lets_move

    * Script that moves all files beginning with an uppercase letter to the directory /tmp/u

17. 101-clean_emacs

    * Script that deletes all files in the current working directory that end with the character ~

18. 102-tree

    * Script that creates the directories welcome/, welcome/to/ and welcome/to/school/

19. 103-commas

    * Script that displays lists of files and directories end with a slash, start with a dot, separeted by commas and orderedin alpha except .and ..

20. school.mgc

    * : 0 string SCHOOL School data !:mime school Create a magic file called school.mgc that can be used with the command file to detect School data files. School  data files always contain "SCHOOL" at offset 0.

    Additional

    From what I understand, the magic file is used to detect patterns in files and will give a specified output depending on a matching pattern. The first argument is a number representing the offset. The second argument is the data type you are searching for. In our case, it is a string. The third argument is the data you are searching for. In our case, "SCHOOL", which we specified as a string in the second argument. The fourth argument is the message you want to output on match. If the search matches, it will output this message. The last argument is separated by a line. Since the fourth argument can be long and contain multiple strings, we separate the fourth and fifth arguments with this new line. This last argument can be multiple different things. In this case, a MIME type. According to bash manual, a "MIME type is given on a separate line, which must be the next non-blank or comment line after the magic line that identifies the file type". I knew to search for a MIME type because the example provided: $ file --mime-type -m school.mgc * The above returns message "School" when matching a MIME ?? Not exactly sure, but this is what I can tell from what I've tested out and can see from the output and examples. $ file -m school.mgc * The above will return message "School data" for any offset 0 "SCHOOL" matches. A cool thing to note is that the file command is compiling and running the magic file. So there is no need to compile to magic "permanently". NOTE: Compiling a magic source file: $ file -C -m .mgc This produces the compiled magic file. $ file -i -m .mgc * This allows you to use the compiled file by specifying its name using the -m switch again.



    [Creating a custom magic file](http://cweiske.de/tagebuch/custom-magic-db.htm)
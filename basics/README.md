# Shell, basics

* [Task 0](./0-current_working_directory): Write a script that prints the absolute path name of the current working directory.
  ```
  pwd
  ```

* [Task 1](./1-listit): Display the contents list of your current directory.
  ```
  ls
  ```
* [Task 2](./2-bring_me_home): Write a script that changes the working directory to the user’s home directory.

  * You are not allowed to use any shell variables
    
  ```
  cd
  ```
  
* [Task 3](./3-listfiles): Display current directory contents in a long format.
  ```
  ls -l
  ```
  
* [Task 4](./4-listmorefiles): Display current directory contents, including hidden files (starting with .). Use the long format.
  ```
  ls -l -a
  ```
  
* [Task 5](./5-listfilesdigitonly): Display current directory contents.

  * Long format
  * with user and group IDs displayed numerically
  * And hidden files (starting with .)
  ```
  ls -na
  ```
  
* [Task 6](./6-firstdirectory): Create a script that creates a directory named my_first_directory in the /tmp/ directory.
  ```
  mkdir /tmp/my_first_directory
  ```
  
* [Task 7](./7-movethatfile): Move the file betty from /tmp/ to /tmp/my_first_directory.
  ```
  mv /tmp/betty /tmp/my_first_directory
  ```
  
* [Task 8](./8-firstdelete): Delete the file betty.

  * The file betty is in /tmp/my_first_directory
  ```
  rm /tmp/my_first_directory/betty
  ```
  
  * [Task 9](./9-firstdirdeletion): Delete the directory my_first_directory that is in the /tmp directory.
  ```
  rmdir /tmp/my_first_directory
  ```
  
  * [Task 10](./10-back): Write a script that changes the working directory to the previous one.
  ```
  cd -
  ```
  
  * [Task 11](./11-lists): Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the /boot directory (in this order), in long format.

     Be careful with the /
  ```
  ls -la . .. /boot
  ```
  
  * [Task 12](./12-file_type): Write a script that prints the type of the file named iamafile. The file iamafile will be in the /tmp directory when we will run your script.
  ```
  file /tmp/iamafile
  ```
  
  * [Task 13](./13-symbolic_link): Create a symbolic link to /bin/ls, named __ls__. The symbolic link should be created in the current working directory.
  ```
  ln -s /bin/ls __ls__
  ```
  
  * [Task 14](./14-copy_html): Create a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.

     You can consider that all HTML files have the extension .html
  ```
  cp -n *html ..
  ```
  
  * [Task 15](./15-lets_move): Create a script that moves all files beginning with an uppercase letter to the directory /tmp/u.

     You can assume that the directory /tmp/u will exist when we will run your script
  ```
  mv [[:upper:]]* /tmp/u
  ```
  
  * [Task 16](./16-clean_emacs): Create a script that deletes all files in the current working directory that end with the character ~.
  ```
  rm *~ 
  ```
  
  * [Task 17](./17-tree): Create a script that creates the directories welcome/, welcome/to/ and welcome/to/school in the current directory.

     You are only allowed to use two spaces (and lines) in your script, not more.
  ```
  mkdir -p welcome/to/school
  ```

### By Anthony Goutieras
  Weekly project from 10/10/25 to 19/10/25 for Holberton School Bordeaux

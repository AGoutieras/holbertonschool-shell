# Shell, basics

* [Task 0](./0-current_working_directory): Write a script that prints the absolute path name of the current working directory.
  <details>
    <summary>Show answer</summary>

    ```
    pwd
    ```
  </details>

* [Task 1](./1-listit): Display the contents list of your current directory.
  <details>
    <summary>Show answer</summary>

    ```
    ls
    ```
  </details>
  
* [Task 2](./2-bring_me_home): Write a script that changes the working directory to the user’s home directory.

  * You are not allowed to use any shell variables
    
  <details>
    <summary>Show answer</summary>

    ```
    cd
    ```
  </details>
  
* [Task 3](./3-listfiles): Display current directory contents in a long format.
  <details>
    <summary>Show answer</summary>

    ```
    ls -l
    ```
  </details>
  
* [Task 4](./4-listmorefiles): Display current directory contents, including hidden files (starting with $${\color{red}.}$$). Use the long format.
  <details>
    <summary>Show answer</summary>

    ```
    ls -l -a
    ```
  </details>
  
* [Task 5](./5-listfilesdigitonly): Display current directory contents.

  * Long format
  * with user and group IDs displayed numerically
  * And hidden files (starting with .)
  <details>
    <summary>Show answer</summary>

    ```
    ls -na
    ```
  </details>
  
* [Task 6](./6-firstdirectory): Create a script that creates a directory named $${\color{red}my\\_first\\_directory}$$ in the $${\color{red}/tmp/}$$ directory.
  <details>
    <summary>Show answer</summary>

    ```
    mkdir /tmp/my_first_directory
    ```
  </details>
  
* [Task 7](./7-movethatfile): Move the file $${\color{red}betty}$$ from $${\color{red}/tmp/}$$ to $${\color{red}/tmp/my\\_first\\_directory}$$.
  <details>
    <summary>Show answer</summary>

    ```
    mv /tmp/betty /tmp/my_first_directory
    ```
  </details>
  
* [Task 8](./8-firstdelete): Delete the file $${\color{red}betty}$$.

  * The file $${\color{red}betty}$$ is in $${\color{red}/tmp/my\\_first\\_directory}$$
  <details>
    <summary>Show answer</summary>

    ```
    rm /tmp/my_first_directory/betty
    ```
  </details>
  
* [Task 9](./9-firstdirdeletion): Delete the directory $${\color{red}my\\_first\\_directory}$$ that is in the $${\color{red}/tmp}$$ directory.
  <details>
    <summary>Show answer</summary>

    ```
    rmdir /tmp/my_first_directory
    ```
  </details>
  
* [Task 10](./10-back): Write a script that changes the working directory to the previous one.
  <details>
    <summary>Show answer</summary>

    ```
    cd -
    ```
  </details>
  
* [Task 11](./11-lists): Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the $${\color{red}/boot}$$ directory (in this order), in long format.

     Be careful with the $${\color{red}/}$$
  <details>
    <summary>Show answer</summary>

    ```
    ls -la . .. /boot
    ```
  </details>
  
* [Task 12](./12-file_type): Write a script that prints the type of the file named $${\color{red}iamafile}$$. The file $${\color{red}iamafile}$$ will be in the $${\color{red}/tmp}$$ directory when we will run your script.
  <details>
    <summary>Show answer</summary>

    ```
    file /tmp/iamafile
    ```
  </details>
  
* [Task 13](./13-symbolic_link): Create a symbolic link to $${\color{red}/bin/ls}$$, named $${\color{red}\\\_\\\_ls\\\_\\\_}$$ . The symbolic link should be created in the current working directory.
  <details>
    <summary>Show answer</summary>

    ```
    ln -s /bin/ls __ls__
    ```
  </details>
  
* [Task 14](./14-copy_html): Create a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.

     You can consider that all HTML files have the extension $${\color{red}.html}$$
  <details>
    <summary>Show answer</summary>

    ```
    cp -n *html ..
    ```
  </details>
  
* [Task 15](./15-lets_move): Create a script that moves all files beginning with an uppercase letter to the directory $${\color{red}/tmp/u}$$.

     You can assume that the directory $${\color{red}/tmp/u}$$ will exist when we will run your script
  <details>
    <summary>Show answer</summary>

    ```
    mv [[:upper:]]* /tmp/u
    ```
  </details>
  
* [Task 16](./16-clean_emacs): Create a script that deletes all files in the current working directory that end with the character $${\color{red}{\sim}}$$.
  <details>
    <summary>Show answer</summary>

    ```
    rm *~ 
    ```
  </details>
  
* [Task 17](./17-tree): Create a script that creates the directories $${\color{red}welcome/}$$, $${\color{red}welcome/to/}$$ and $${\color{red}welcome/to/school}$$ in the current directory.

     You are only allowed to use two spaces (and lines) in your script, not more.
  <details>
    <summary>Show answer</summary>

    ```
    mkdir -p welcome/to/school
    ```
  </details>

### By $${\color{red}Anthony \space Goutieras}$$
  Weekly project from 10/10/25 to 19/10/25 for Holberton School Bordeaux

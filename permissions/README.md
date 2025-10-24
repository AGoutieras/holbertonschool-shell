# Shell, permissions

* [Task 0](./0-iam_betty): Create a script that switches the current user to the user $${\color{red}betty}$$.

  * You should use exactly 8 characters for your command (+1 character for the new line)
  * You can assume that the user $${\color{red}betty}$$ will exist when we will run your script
  <details>
    <summary>Show answer</summary>

    ```
    su betty
    ```
  </details>

* [Task 1](./1-who_am_i): Write a script that prints the effective username of the current user.
  <details>
    <summary>Show answer</summary>

  ```
  whoami
  ```
  </details>

* [Task 2](./2-groups): Write a script that prints all the groups the current user is part of.
  <details>
    <summary>Show answer</summary>

  ```
  groups
  ```
  </details>

* [Task 3](./3-new_owner): Write a script that changes the owner of the file $${\color{red}hello}$$ to the user $${\color{red}betty}$$.
  <details>
    <summary>Show answer</summary>

  ```
  chown betty hello
  ```
  </details>

* [Task 4](./4-empty): Write a script that creates an empty file called $${\color{red}hello}$$.
  <details>
    <summary>Show answer</summary>

  ```
  touch hello
  ```
  </details>

* [Task 5](./5-execute): Write a script that adds execute permission to the owner of the file $${\color{red}hello}$$.

  * The file $${\color{red}hello}$$ will be in the working directory
  <details>
    <summary>Show answer</summary>

  ```
  chmod 744 hello
  ```
  </details>

* [Task 6](./6-multiple_permissions): Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file $${\color{red}hello}$$.

  * The file $${\color{red}hello}$$ will be in the working directory
  <details>
    <summary>Show answer</summary>

  ```
  chmod 754 hello
  ```
  </details>

* [Task 7](./7-everybody): Write a script that adds execution permission to the owner, the group owner and the other users, to the file $${\color{red}hello}$$

  * The file $${\color{red}hello}$$ will be in the working directory
  * You are not allowed to use commas for this script
  <details>
    <summary>Show answer</summary>

  ```
  chmod a+x hello
  ```
  </details>

* [Task 8](./8-James_Bond): Write a script that sets the permission to the file $${\color{red}hello}$$ as follows:

  * Owner: no permission at all
  * Group: no permission at all
  * Other users: all the permissions
The file $${\color{red}hello}$$ will be in the working directory You are not allowed to use commas for this script
  <details>
    <summary>Show answer</summary>

  ```
  chmod 007 hello
  ```
  </details>

* [Task 9](./9-John_Doe): Write a script that sets the mode of the file $${\color{red}hello}$$ to this: 

  ```
  -rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
  ```
    * The file $${\color{red}hello}$$ will be in the working directory
    * You are not allowed to use commas for this script
  <details>
    <summary>Show answer</summary>

  ```
  chmod 753 hello
  ```
  </details>

* [Task 10](./10-mirror_permissions): Write a script that sets the mode of the file $${\color{red}hello}$$ the same as $${\color{red}olleh}$$ ’s mode.
     * The file $${\color{red}hello}$$ will be in the working directory
     * The file $${\color{red}olleh}$$ will be in the working directory
  <details>
    <summary>Show answer</summary>

  ```
  chmod --reference olleh hello
  ```
  </details>

* [Task 11](./11-directories_permissions): Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed.
  <details>
    <summary>Show answer</summary>

  ```
  chmod -R a+X .
  ```
  </details>

* [Task 12](./12-directory_permissions): Create a script that creates a directory called $${\color{red}my_dir}$$ with permissions 751 in the working directory.
  <details>
    <summary>Show answer</summary>

  ```
  mkdir -m 751 my_dir
  ```
  </details>

* [Task 13](./13-change_group): Write a script that changes the group owner to $${\color{red}school}$$ for the file $${\color{red}hello}$$

    * The file $${\color{red}hello}$$ will be in the working directory
    * **The script must be present on the github repository and on the sandbox on the folder /tmp**
  <details>
    <summary>Show answer</summary>

  ```
  chgrp school hello
  ```
  </details>

* [Task 14](./14-change_owner_and_group): Write a script that changes the owner to $${\color{red}vincent}$$ and the group owner to $${\color{red}staff}$$ for all the files and directories in the working directory.
  <details>
    <summary>Show answer</summary>

  ```
  chown -R vincent:staff .
  ```
  </details>

* [Task 15](./15-symbolic_link_permissions): Write a script that changes the owner and the group owner of $${\color{red}\\_hello}$$ to $${\color{red}vincent}$$ and $${\color{red}staff}$$ respectively.

    * The file $${\color{red}\\_hello}$$ is in the working directory
    * The file $${\color{red}\\_hello}$$ is a symbolic link
  <details>
    <summary>Show answer</summary>

  ```
  chown -h vincent:staff _hello
  ```
  </details>

* [Task 16](./16-if_only): Write a script that changes the owner of the file $${\color{red}hello}$$ to $${\color{red}vincent}$$ only if it is owned by the user $${\color{red}guillaume}$$.

    * The file $${\color{red}hello}$$ will be in the working directory
  <details>
    <summary>Show answer</summary>

  ```
  chown --from=guillaume vincent hello
  ```
  </details>

### By $${\color{red}Anthony \space Goutieras}$$
  Weekly project from 10/10/25 to 19/10/25 for Holberton School Bordeaux

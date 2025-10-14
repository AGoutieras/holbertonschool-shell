# Shell, permissions

* [Task 0](./0-iam_betty): Create a script that switches the current user to the user betty.

  * You should use exactly 8 characters for your command (+1 character for the new line)
  * You can assume that the user betty will exist when we will run your script
  ```
  su betty
  ```

* [Task 1](./1-who_am_i): Write a script that prints the effective username of the current user.
  ```
  whoami
  ```

* [Task 2](./2-groups): Write a script that prints all the groups the current user is part of.
  ```
  groups
  ```

* [Task 3](./3-new_owner): Write a script that changes the owner of the file hello to the user betty.
  ```
  chown betty hello
  ```

* [Task 4](./4-empty): Write a script that creates an empty file called hello.
  ```
  touch hello
  ```

* [Task 5](./5-execute): Write a script that adds execute permission to the owner of the file hello.

  * The file hello will be in the working directory
  ```
  chmod 744 hello
  ```

* [Task 6](./6-multiple_permissions): Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.

  * The file hello will be in the working directory
  ```
  chmod 754 hello
  ```

* [Task 7](./7-everybody): Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello

  * The file hello will be in the working directory
  * You are not allowed to use commas for this script
  ```
  chmod a+x hello
  ```

* [Task 8](./8-James_Bond): Write a script that sets the permission to the file hello as follows:

  * Owner: no permission at all
  * Group: no permission at all
  * Other users: all the permissions
The file hello will be in the working directory You are not allowed to use commas for this script
  ```
  chmod 007 hello
  ```

* [Task 9](./9-John_Doe): Write a script that sets the mode of the file hello to this: 
            ```
            -rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
            ```
  * The file hello will be in the working directory
  * You are not allowed to use commas for this script
  ```
  chmod 753 hello
  ```

* [Task 10](./10-mirror_permissions): The file hello will be in the working directory
  * You are not allowed to use commas for this script
  ```
  chmod --reference olleh hello
  ```

* [Task 11](./11-directories_permissions): Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed.
  ```
  chmod -R a+X .
  ```

* [Task 12](./12-directory_permissions): Create a script that creates a directory called my_dir with permissions 751 in the working directory.
  ```
  mkdir -m 751 my_dir
  ```

* [Task 13](./13-change_group): Write a script that changes the group owner to school for the file hello

  * The file hello will be in the working directory
  * **The script must be present on the github repository and on the sandbox on the folder /tmp**
  ```
  chgrp school hello
  ```

* [Task 14](./14-change_owner_and_group): Write a script that changes the owner to vincent and the group owner to staff for all the files and directories in the working directory.
  ```
  chown -R vincent:staff .
  ```

* [Task 15](./15-symbolic_link_permissions): Write a script that changes the owner and the group owner of _hello to vincent and staff respectively.

  * The file _hello is in the working directory
  * The file _hello is a symbolic link
  ```
  chown -h vincent:staff _hello
  ```

* [Task 16](./16-if_only): Write a script that changes the owner of the file hello to vincent only if it is owned by the user guillaume.

  * The file hello will be in the working directory
  ```
  chown --from=guillaume vincent hello
  ```

### By Anthony Goutieras
  Weekly project from 10/10/25 to 19/10/25 for Holberton School Bordeaux

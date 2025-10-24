# Shell, I/O Redirections and filters

* [Task 0](./0-hello_world): Write a script that prints “Hello, World”, followed by a new line to the standard output.
  <details>
    <summary>Show answer</summary>

    ```
    echo Hello, World
    ```
  </details>

* [Task 1](./1-confused_smiley): Write a script that displays a confused smiley $${\color{red}"(Ôo)'}$$.
  <details>
    <summary>Show answer</summary>

    ```
    echo "\"(Ôo)'"
    ```
  </details>

* [Task 2](./2-hellofile): Display the content of the $${\color{red}/etc/passwd}$$ file.
  <details>
    <summary>Show answer</summary>

    ```
    cat /etc/passwd
    ```
  </details>

* [Task 3](./3-twofiles): Display the content of $${\color{red}/etc/passwd}$$ and $${\color{red}/etc/hosts}$$
  <details>
    <summary>Show answer</summary>

    ```
    cat /etc/passwd /etc/hosts
    ```
  </details>

* [Task 4](./4-lastlines): Display the last 10 lines of $${\color{red}/etc/passwd}$$
  <details>
    <summary>Show answer</summary>

    ```
    tail /etc/passwd
    ```
  </details>

* [Task 5](./5-firstlines): Display the first 10 lines of $${\color{red}/etc/passwd}$$
  <details>
    <summary>Show answer</summary>

    ```
    head /etc/passwd
    ```
  </details>

* [Task 6](./6-third_line): Write a script that displays the third line of the file $${\color{red}iacta}$$.

  The file $${\color{red}iacta}$$ will be in the working directory

  * You’re not allowed to use $${\color{red}sed}$$
  <details>
    <summary>Show answer</summary>

    ```
    head -n 3 iacta | tail -n 1
    ```
  </details>

* [Task 7](./7-file): Write a shell script that creates a file named exactly $${\color{red}\backslash * \backslash \backslash '"Best \space School" \backslash ' \backslash \backslash *\\$ \backslash ? \backslash * \backslash * \backslash * \backslash * \backslash * :)}$$ containing the text Best School ending by a new line.
  <details>
    <summary>Show answer</summary>

    ```
    echo -e "Best School"  >> "\\*\\\\'\"Best School\"\\'\\\\*$\\?\\*\\*\\*\\*\\*:)"
    ```
  </details>

* [Task 8](./8-cwd_state): Write a script that writes into the file $${\color{red}ls\\_cwd\\_content}$$ the result of the command $${\color{red}ls \space -la}$$. If the file $${\color{red}ls\\_cwd\\_content}$$ already exists, it should be overwritten. If the file $${\color{red}ls\\_cwd\\_content}$$ does not exist, create it.
  <details>
    <summary>Show answer</summary>

    ```
    ls -la > ls_cwd_content
    ```
  </details>

* [Task 9](./9-duplicate_last_line): Write a script that duplicates the last line of the file $${\color{red}iacta}$$

  * The file $${\color{red}iacta}$$ will be in the working directory
  <details>
    <summary>Show answer</summary>

    ```
    tail -1 iacta >> iacta 
    ```
  </details>

* [Task 10](./10-no_more_js): Write a script that deletes all the regular files (not the directories) with a $${\color{red}.js}$$ extension that are present in the current directory and all its subfolders.
  <details>
    <summary>Show answer</summary>

    ```
    find . -type f -name '*.js' -delete
    ```
  </details>

* [Task 11](./11-directories): Write a script that counts the number of directories and sub-directories in the current directory.

  * The current and parent directories should not be taken into account
  * Hidden directories should be counted
  <details>
    <summary>Show answer</summary>

    ```
    find -mindepth 1 -type d | wc -l
    ```
  </details>

* [Task 12](./12-newest_files): Create a script that displays the 10 newest files in the current directory.

  Requirements:

  * One file per line
  * Sorted from the newest to the oldest
  <details>
    <summary>Show answer</summary>

    ```
    ls -t | head -n 10
    ```
  </details>

* [Task 13](./13-unique): Create a script that takes a list of words as input and prints only words that appear exactly once.

  * Input format: One line, one word
  * Output format: One line, one word
  * Words should be sorted
  <details>
    <summary>Show answer</summary>

    ```
    sort | uniq -u
    ```
  </details>

* [Task 14](./14-findthatword): Display lines containing the pattern “root” from the file $${\color{red}/etc/passwd}$$
  <details>
    <summary>Show answer</summary>

    ```
    grep root /etc/passwd
    ```
  </details>

* [Task 15](./15-countthatword): Display the number of lines that contain the pattern “bin” in the file $${\color{red}/etc/passwd}$$
  <details>
    <summary>Show answer</summary>

    ```
    grep -c bin /etc/passwd
    ```
  </details>

* [Task 16](./16-whatsnext): Display lines containing the pattern “root” and 3 lines after them in the file $${\color{red}/etc/passwd}$$.
  <details>
    <summary>Show answer</summary>

    ```
    grep -A 3 root /etc/passwd
    ```
  </details>

* [Task 17](./17-hidethisword): Display all the lines in the file $${\color{red}/etc/passwd}$$ that do not contain the pattern “bin”.
  <details>
    <summary>Show answer</summary>

    ```
    grep -v bin /etc/passwd
    ```
  </details>

* [Task 18](./18-letteronly): Display all lines of the file $${\color{red}/etc/ssh/sshd\\_config}$$ starting with a letter.

  * include capital letters as well
  <details>
    <summary>Show answer</summary>

    ```
    grep "^[a-zA-z]" /etc/ssh/sshd_config
    ```
  </details>

* [Task 19](./19-AZ): Replace all characters $${\color{red}A}$$ and $${\color{red}c}$$ from input to $${\color{red}Z}$$ and $${\color{red}e}$$ respectively.
  <details>
    <summary>Show answer</summary>

    ```
    tr 'Ac' 'Ze'
    ```
  </details>

* [Task 20](./20-hiago): Create a script that removes all letters $${\color{red}c}$$ and $${\color{red}C}$$ from input.
  <details>
    <summary>Show answer</summary>

    ```
    tr -d 'cC'
    ```
  </details>

* [Task 21](./21-reverse): Write a script that reverse its input.
  <details>
    <summary>Show answer</summary>

    ```
    rev
    ```
  </details>

* [Task 22](./22-users_and_homes): Write a script that displays all users and their home directories, sorted by users.

  * Based on the the $${\color{red}/etc/passwd}$$ file
  <details>
    <summary>Show answer</summary>

    ```
    cut -d : -f 1,6 /etc/passwd | sort
    ```
  </details>

* [Task 23](./23-empty_casks): Write a command that finds all empty files and directories in the current directory and all sub-directories.

  * Only the names of the files and directories should be displayed (not the entire path)
  * Hidden files should be listed
  * One file name per line
  * The listing should end with a new line
  * You are not allowed to use $${\color{red}basename}$$, $${\color{red}grep}$$, $${\color{red}egrep}$$, $${\color{red}fgrep}$$ or $${\color{red}rgrep}$$
  <details>
    <summary>Show answer</summary>

    ```
    find . -empty -printf %f'\n'
    ```
  </details>

* [Task 24](./24-gifs): Write a script that lists all the files with a $${\color{red}.gif}$$ extension in the current directory and all its sub-directories.

  * Hidden files should be listed
  * Only regular files (not directories) should be listed
  * The names of the files should be displayed without their extensions
  * The files should be sorted by byte values, but case-insensitive (file $${\color{red}aaa}$$ should be listed before file $${\color{red}bbb}$$, file $${\color{red}.b}$$ should be listed before file $${\color{red}a}$$, and file $${\color{red}Rona}$$ should be listed after file $${\color{red}jay}$$)
  * One file name per line
  * The listing should end with a new line
  * You are not allowed to use $${\color{red}basename}$$, $${\color{red}grep}$$, $${\color{red}egrep}$$, $${\color{red}fgrep}$$ or $${\color{red}rgrep}$$
  <details>
    <summary>Show answer</summary>

    ```
    
    ```
  </details>

* [Task 25](./25-acrostic): An acrostic is a poem (or other form of writing) in which the first letter (or syllable, or word) of each line (or paragraph, or other recurring feature in the text) spells out a word, message or the alphabet. The word comes from the French acrostiche from post-classical Latin acrostichis). As a form of constrained writing, an acrostic can be used as a mnemonic device to aid memory retrieval. [Read more](https://en.wikipedia.org/wiki/Acrostic).

  Create a script that decodes acrostics that use the first letter of each line.

  * The ‘decoded’ message has to end with a new line
  * You are not allowed to use $${\color{red}grep}$$, $${\color{red}egrep}$$, $${\color{red}fgrep}$$ or $${\color{red}rgrep}$$
  <details>
    <summary>Show answer</summary>

    ```
    cut -c 1 | paste -s -d ' ' | tr -d ' '
    ```
  </details>

* [Task 26](./26-the_biggest_fan): Write a script that parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests.

  * Order by number of requests, most active host or IP at the top
  * You are not allowed to use $${\color{red}grep}$$, $${\color{red}egrep}$$, $${\color{red}fgrep}$$ or $${\color{red}rgrep}$$
  <details>
    <summary>Show answer</summary>

    ```
    
    ```
  </details>

### By $${\color{red}Anthony \space Goutieras}$$
  Weekly project from 10/10/25 to 19/10/25 for Holberton School Bordeaux

# Shell, init files, variables and expansions

* [Task 0](./0-alias):Create a script that creates an alias.

  * Name: $${\color{red}ls}$$
  * Value: $${\color{red}rm -f *}$$
  <details>
    <summary>Show answer</summary>

    ```
    alias ls="rm -f *"
    ```

* [Task 1](./1-hello_you): Create a script that prints $${\color{red}hello \space user}$$, where user is the current Linux user.
  <details>
    <summary>Show answer</summary>

    ```
    echo hello $USER
    ```

* [Task 2](./2-path): Add $${\color{red}/action}$$ to the $${\color{red}PATH}$$. $${\color{red}/action}$$ should be the last directory the shell looks into when looking for a program.
  <details>
    <summary>Show answer</summary>

    ```
    PATH=$PATH:/action
    ```

* [Task 3](./3-paths): Create a script that counts the number of directories in the $${\color{red}PATH}$$.
  <details>
    <summary>Show answer</summary>

    ```
    echo "$PATH" | tr ':' '\n' | grep -v '^$' | wc -l
    ```

* [Task 4](./4-global_variables): Create a script that lists environment variables.
  <details>
    <summary>Show answer</summary>

    ```
    printenv
    ```

* [Task 5](./5-local_variables): Create a script that lists all local variables and environment variables, and functions.
  <details>
    <summary>Show answer</summary>

    ```
    set
    ```

* [Task 6](./6-create_local_variable): Create a script that creates a new local variable.

  * Name: $${\color{red}BEST}$$
  * Value: $${\color{red}School}$$
  <details>
    <summary>Show answer</summary>

    ```
    BEST=School
    ```

* [Task 7](./7-create_global_variable): Create a script that creates a new global variable.

  * Name: $${\color{red}BEST}$$
  * Value: $${\color{red}School}$$
  <details>
    <summary>Show answer</summary>

    ```
    export BEST=School
    ```

* [Task 8](./8-true_knowledge): Write a script that prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.
  <details>
    <summary>Show answer</summary>

    ```
    echo $((TRUEKNOWLEDGE + 128))
    ```

* [Task 9](./9-divide_and_rule): Write a script that prints the result of $${\color{red}POWER}$$ divided by $${\color{red}DIVIDE}$$, followed by a new line.

  * $${\color{red}POWER}$$ and $${\color{red}DIVIDE}$$ are environment variables
  <details>
    <summary>Show answer</summary>

    ```
    echo $((POWER / DIVIDE))
    ```

* [Task 10](./10-love_exponent_breath): Write a script that displays the result of $${\color{red}BREATH}$$ to the power $${\color{red}LOVE}$$

  * $${\color{red}BREATH}$$ and $${\color{red}LOVE}$$ are environment variables
  * The script should display the result, followed by a new line
  <details>
    <summary>Show answer</summary>

    ```
    echo $((BREATH ** LOVE))
    ```

* [Task 11](./11-binary_to_decimal): Write a script that converts a number from base 2 to base 10.

  * The number in base 2 is stored in the environment variable $${\color{red}BINARY}$$
  * The script should display the number in base 10, followed by a new line
  <details>
    <summary>Show answer</summary>

    ```
    echo $((2#$BINARY))
    ```

* [Task 12](./12-combinations): Create a script that prints all possible combinations of two letters, except $${\color{red}oo}$$.

  * Letters are lower cases, from $${\color{red}a}$$ to $${\color{red}z}$$
  * One combination per line
  * The output should be alpha ordered, starting with $${\color{red}aa}$$
  * Do not print $${\color{red}oo}$$
  * Your script file should contain maximum 64 characters
  <details>
    <summary>Show answer</summary>

    ```
    printf '%s\n' {a..z}{a..z} | grep -v oo
    ```

* [Task 13](./13-print_float): Write a script that prints a number with two decimal places, followed by a new line.

  The number will be stored in the environment variable $${\color{red}NUM}$$.
  <details>
    <summary>Show answer</summary>

    ```
    printf "%.2f\n" "$NUM"
    ```

* [Task 14](./14-decimal_to_hexadecimal): Write a script that converts a number from base 10 to base 16.

  * The number in base 10 is stored in the environment variable $${\color{red}DECIMAL}$$
  * The script should display the number in base 16, followed by a new line
  <details>
    <summary>Show answer</summary>

    ```
    printf "%x\n" $DECIMAL
    ```

* <ins>Task 15</ins>: Write a blog post describing step by step what happens when you type $${\color{red}ls *.c}$$ and hit Enter in your shell. Try to explain every step you know of, and give examples. A total beginner should understand what you have written.

  * Have at least one picture, at the top of the blog post
  * Publish your blog post on Medium or LinkedIn
  * Share your blog post at least on LinkedIn
  * Write professionally and intelligibly
  * Please, remember that these blogs must be written in English to further your technical ability in a variety of settings
**Remember, future employers will see your articles; take this seriously, and produce something that will be an asset to your future**

* [Task 16](./15-rot13): Write a script that encodes and decodes text using the rot13 encryption. Assume ASCII.
  <details>
    <summary>Show answer</summary>

    ```
    tr 'A-Za-z' 'N-ZA-Mn-za-m'
    ```

* [Task 17](./16-odd): Write a script that prints every other line from the input, starting with the first line.
  <details>
    <summary>Show answer</summary>

    ```
  
    ```

* [Task 18](./17-water_and_stir): Write a shell script that adds the two numbers stored in the environment variables $${\color{red}WATER}$$ and $${\color{red}STIR}$$ and prints the result.

  * WATER is in base water
  * STIR is in base stir.
  * The result should be in base bestchol
  <details>
    <summary>Show answer</summary>

    ```
  
    ```

### By $${\color{red}Anthony \space Goutieras}$$
  Weekly project from 10/10/25 to 19/10/25 for Holberton School Bordeaux

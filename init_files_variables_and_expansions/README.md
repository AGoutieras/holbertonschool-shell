# Shell, init files, variables and expansions

* [Task 0](./0-alias):Create a script that creates an alias.

  * Name: ls
  * Value: rm -f *
  ```
  alias ls="rm -f *"
  ```

* [Task 1](./1-hello_you): Create a script that prints hello user, where user is the current Linux user.
  ```
  echo hello $USER
  ```

* [Task 2](./2-path): Add /action to the PATH. /action should be the last directory the shell looks into when looking for a program.
  ```
  PATH=$PATH:/action
  ```

* [Task 3](./3-paths): Create a script that counts the number of directories in the PATH.
  ```
  echo "$PATH" | tr ':' '\n' | grep -v '^$' | wc -l
  ```

* [Task 4](./4-global_variables): Create a script that lists environment variables.
  ```
  printenv
  ```

* [Task 5](./5-local_variables): Create a script that lists all local variables and environment variables, and functions.
  ```
  set
  ```

* [Task 6](./6-create_local_variable): Create a script that creates a new local variable.

  * Name: BEST
  * Value: School
  ```
  BEST=School
  ```

* [Task 7](./7-create_global_variable): Create a script that creates a new global variable.

  * Name: BEST
  * Value: School
  ```
  export BEST=School
  ```

* [Task 8](./8-true_knowledge): Write a script that prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.
  ```
  echo $((TRUEKNOWLEDGE + 128))
  ```

* [Task 9](./9-divide_and_rule): Write a script that prints the result of POWER divided by DIVIDE, followed by a new line.

  * POWER and DIVIDE are environment variables
  ```
  echo $((POWER / DIVIDE))
  ```

* [Task 10](./10-love_exponent_breath): Write a script that displays the result of BREATH to the power LOVE

  * BREATH and LOVE are environment variables
  * The script should display the result, followed by a new line
  ```
  echo $((BREATH ** LOVE))
  ```

* [Task 11](./11-binary_to_decimal): Write a script that converts a number from base 2 to base 10.

  * The number in base 2 is stored in the environment variable BINARY
  * The script should display the number in base 10, followed by a new line
  ```
  echo $((2#$BINARY))
  ```

* [Task 12](./12-combinations): Create a script that prints all possible combinations of two letters, except oo.

  * Letters are lower cases, from a to z
  * One combination per line
  * The output should be alpha ordered, starting with aa
  * Do not print oo
  * Your script file should contain maximum 64 characters
  ```
  printf '%s\n' {a..z}{a..z} | grep -v oo
  ```

* [Task 13](./13-print_float): Write a script that prints a number with two decimal places, followed by a new line.

  The number will be stored in the environment variable NUM.
  ```
  printf "%.2f\n" "$NUM"
  ```

* [Task 14](./14-decimal_to_hexadecimal): Write a script that converts a number from base 10 to base 16.

  * The number in base 10 is stored in the environment variable DECIMAL
  * The script should display the number in base 16, followed by a new line
  ```
  printf "%x\n" $DECIMAL
  ```

* <ins>Task 15</ins>: Write a blog post describing step by step what happens when you type ls *.c and hit Enter in your shell. Try to explain every step you know of, and give examples. A total beginner should understand what you have written.

  * Have at least one picture, at the top of the blog post
  * Publish your blog post on Medium or LinkedIn
  * Share your blog post at least on LinkedIn
  * Write professionally and intelligibly
  * Please, remember that these blogs must be written in English to further your technical ability in a variety of settings
**Remember, future employers will see your articles; take this seriously, and produce something that will be an asset to your future**

* [Task 16](./15-rot13): Write a script that encodes and decodes text using the rot13 encryption. Assume ASCII.
  ```
  
  ```

* [Task 17](./16-odd): Write a script that prints every other line from the input, starting with the first line.
  ```
  
  ```

* [Task 18](./17-water_and_stir): Write a shell script that adds the two numbers stored in the environment variables WATER and STIR and prints the result.

  * WATER is in base water
  * STIR is in base stir.
  * The result should be in base bestchol
  ```
  
  ```

# Command Chaining and Scripting

## Chaining With semicolons - Challenge 1
### This challenge requires us to use the semicolon (`;`) operator to execute two commands sequentially, regardless of the first command's success.

**Flag:** `pwn.college{INUrvAcWhcsXW-BakhoGTlv4-xc.QX1UDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
bash
hacker@terminal-multiplexing~switching-windows-tmux:~$ 
Connected!
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn;/challenge/college
Yes! You chained /challenge/pwn and /challenge/college!
```

## What I Learned
The challenge taught me how to use the semicolon (;) operator to chain multiple commands, ensuring they all execute one after the other.

## References
None

## Building On Success - Challenge 2

### This challenge requires us to use the logical AND operator (&&) to execute a second command only if the first command succeeds (exits with a zero status).
**Flag**: `pwn.college{AfPmOrdWYVtrW1IeYfNtsdhvuGW.0lM0MDOxwyN4gjNzEzW}`

```
The process of obtaining the flag involved:

hacker@chaining~building-on-success:~$ /challenge/first-success
hacker@chaining~building-on-success:~$ /challenge/second
Error: /challenge/first-success must be successfully chained with
/challenge/second using &&
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second
Nice chaining!
```

## What I Learned
The challenge taught me how to use the logical AND (&&) operator for conditional execution, where the second command runs only upon the success of the first.

## References
None

## Handling Failure - Challenge 3

### This challenge requires us to use the logical OR operator (||) to execute a second command only if the first command fails (exits with a non-zero status).
**Flag**: `pwn.college{obTZcPwqS6Gndgh8rEjtq_An2RZ.01M0MDOxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second
Nice chaining! Flag: pwn.college{obTZcPwqS6Gndgh8rEjtq_An2RZ.01M0MDOxwyN4gjNzEzW}
```

## What I Learned
The challenge taught me how to use the logical OR (||) operator for conditional execution, where the second command runs only upon the failure of the first.

## References
None

## Your First Shell Script - Challenge 4
### This challenge requires us to create a basic shell script using a text editor (nano) and execute it with bash.
**Flag**: `pwn.college{gogij8JXqPyqy4sy3_lDubmWXkT.QXxcDO0wyN4gjNzEzW}`

```
The process of obtaining the flag involved:
hacker@chaining~your-first-shell-script:~$ nano x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script!
```

## What I Learned
The challenge taught me the basic process of creating a text file (x.sh) and executing it as a shell script using the bash interpreter.

## References
None

## Redirecting Script output - Challenge 5
### This challenge requires us to use the pipe operator (|) to redirect the standard output of our script into the standard input of another program (/challenge/solve).
**Flag**: `pwn.college{QQbLDVscRoGfYAtPwKtAsd4gt1h.QX4ETO0wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@chaining~redirecting-script-output:~$ bash script.sh > output
No shenanigans with bash options yet, please!
Just run your script with 'bash x.sh'.
It looks like you are not piping this script out to /challenge/solve!
Remember to pipe the output of your script into /challenge/solve using '|'.
hacker@chaining~redirecting-script-output:~$
hacker@chaining~redirecting-script-output:~$ bash script.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{QQbLDVscRoGfYAtPwKtAsd4gt1h.QX4ETO0wyN4gjNzEzW}
```

## What I Learned
The challenge taught me how to use the pipe (|) operator to chain programs, sending the output of the first command (the script) as input to the second command (/challenge/solve).

## References
None

## Executable Shell Scripts - Challenge 6
### This challenge requires us to make a script executable using the chmod command and then run it directly using the ./ path prefix.
**Flag**: `pwn.college{MhNcAdGz0W6tpzIjZ6gF3n38StX.QX0cjM1wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@chaining~executable-shell-scripts:~$ nano solve.sh
hacker@chaining~executable-shell-scripts:~$ ./solve.sh
bash: ./solve.sh: Permission denied
hacker@chaining~executable-shell-scripts:~$ chmod a+x solve.sh
hacker@chaining~executable-shell-scripts:~$ ./solve.sh
Congratulations on your shell script execution!
```
## What I Learned
The challenge taught me how to use chmod a+x to grant execution permission to a script file, allowing it to be run directly with ./solve.sh instead of bash solve.sh.


## References
None

## Understanding Shebangs - Challenge 7
### This challenge requires us to include a shebang line (#!) in our script to specify the interpreter (/bin/bash or similar) to be used when the script is executed directly.
**Flag**: `pwn.college{gLSoa8R7BBJc8Xs6JNAvYGMV2GM.0VOzMDOxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@chaining~understanding-shebangs:~$ nano solve.sh
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{gLSoa8R7BBJc8Xs6JNAvYGMV2GM.0VOzMDOxwyN4gjNzEzW}
```
## What I Learned
The challenge taught me the purpose of the shebang (#!) line at the beginning of a script: it tells the operating system which program interpreter to use for execution.

## References
None

## Scripting With Arguments - Challenge 8
### This challenge requires us to use positional parameters ($1, $2, etc.) within a shell script to access arguments passed on the command line.
**Flag**: `pwn.college{8TwFwoZ4bkCBhjIS3zhveTtUzuw.0VNzMDOxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@chaining~scripting-with-arguments:~$ nano /home/hacker/solve.sh
hacker@chaining~scripting-with-arguments:~$ bash /home/hacker/solve.sh college pwn
pwn college
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct!
Your script properly reversed the arguments.
```

## What I Learned
The challenge taught me how to use positional parameters (like $1 and $2) within a shell script to read and manipulate command-line arguments.

## References
None

## Scripting With Conditionals - Challenge 9
### This challenge requires us to use an if statement with a conditional test ([ ]) to execute different logic based on a condition, such as comparing an argument to a value.
**Flag**: `pwn.college{E0BPQnXSbppfvfFdpPsHRtpF764.0lNzMDOxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@chaining~scripting-with-conditionals:~$ nano solve.sh
hacker@chaining~scripting-with-conditionals:~$ bash solve.sh pwn
college
hacker@chaining~scripting-with-conditionals:~$ bash solve.sh college
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct!
Your script properly handles all the conditions.
```
## What I Learned
The challenge taught me the basic syntax of shell conditional statements using if/then/fi and the test operator ([ ]) for checking conditions.

## References
None

## Scripting With Default Cases - Challenge 10
### This challenge requires us to use an else clause in an if statement to provide a default action when the initial condition is not met.
**Flag**: `pwn.college{U5XJaL8AwqBDXHih-ZsW87N7fos.01NzMDOxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@chaining~scripting-with-default-cases:~$ nano solve.sh
hacker@chaining~scripting-with-default-cases:~$ bash solve.sh pwn
college
hacker@chaining~scripting-with-default-cases:~$ bash solve.sh pwnn
nope
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Correct!
Your script properly handles the if/else conditions.
```

## What I Learned
The challenge taught me how to implement a default case in scripting logic using the else block to handle all conditions that fall outside the main if check.

## References
None

## Scripting With multiple conditions - Challenge 11
### This challenge requires us to use the elif (else if) structure in a shell script to test multiple conditions sequentially.
**Flag**: `pwn.college{AigtALLu_N6ze6rS_pfI9q1VDGd.0FOzMDOxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@chaining~scripting-with-multiple-conditions:~$ nano solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ bash solve.sh pwn
college
hacker@chaining~scripting-with-multiple-conditions:~$ bash solve.sh hack
the planet
hacker@chaining~scripting-with-multiple-conditions:~$ bash solve.sh leanr
unknown
hacker@chaining~scripting-with-multiple-conditions:~$ bash solve.sh learn
linux
hacker@chaining~scripting-with-multiple-conditions:~$ bash solve.sh foo
unknown
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct!
Your script properly handles all the conditions with elif.
```

## What I Learned
The challenge taught me how to structure an if/elif/else block to test several different conditions in a sequential and organized manner.

## References
None

## Reading Shell Scripts - Challenge 12
### This challenge requires us to use the cat command to read the source code of the execution script (/challenge/run) to discover the required input for a successful outcome.
**Flag**: `pwn.college{M1DKeAZ-5ERknCTnOjxb-1elvVj.0lMwgDOxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{M1DKeAZ-5ERknCTnOjxb-1elvVj.0lMwgDOxwyN4gjNzEzW}
```
## What I Learned
The challenge taught me the crucial skill of reading the source code of a checker program (/challenge/run) to understand its logic and find the specific condition required for success (hack the PLANET).

## References
None
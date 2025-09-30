# Shell Variables

## Printing Variables - Challenge 1
### This challenge requires us to use the echo command to print the variable or output.

**Flag:** `pwn.college{MUKKVkI_biDz9VGCGqNQzTCwbi3.QX3UTN0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{MUKKVkI_biDz9VGCGqNQzTCwbi3.QX3UTN0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to use the echo with arguments to print out statements.

## References

None

## Setting Variables - Challenge 2
### This challenge requires us to set the specified variables to certain values.

**Flag:** `pwn.college{4flOnLttsnWYAknDrIL_dcOE3FX.QX5UTN0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{4flOnLttsnWYAknDrIL_dcOE3FX.QX5UTN0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to set the value of a variable.

## References

None

## Multiword Variables - Challenge 3
### This challenge requires us to set multiword value like a string to a variable.

**Flag:** `pwn.college{QrGoHXFxSJKclzvAjkhD1MEgxDG.QXwYTN0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{QrGoHXFxSJKclzvAjkhD1MEgxDG.QXwYTN0wyN4gjNzEzW}

```

## What I Learned

The challenge taught me on how to set a multiword/string value to a given variable.

## References

None

## Exporting Variables - Challenge 4
### This challenge requires us to use the export command to a variable to get the flag.

**Flag:** `pwn.college{gXj4QEqmrAfTDYnKCL9p2MuusMS.QXyYTN0wyN4gjNzEzW}` 

The process of obtaining the flag involved:
```
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{gXj4QEqmrAfTDYnKCL9p2MuusMS.QXyYTN0wyN4gjNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

## What I Learned

The challenge taught me about a `child process of the shell` and exporting variables.

## References

None

## Printing Exported Variables - Challenge 5
### This challenge requires us to print out two diff variables out of which one is exported and the other is a set variable.

**Flag:** `pwn.college{cAa2z8KAWKYrEObgc_N_hrmdo6R.QX4UTN0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=fd645d1439c999c97576e4cfc89c613eac07a375ad383537ff3ecbb5f651750f
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{cAa2z8KAWKYrEObgc_N_hrmdo6R.QX4UTN0wyN4gjNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

## What I Learned

The challenge taught me on how to call and print out an exported variable properly.

## References

None

## Storing Command outputs - Challenge 6
### This challenge requires us to store the output in a file to obtain the flag.

**Flag:** `pwn.college{8nGBn2tv50q2mGB608-FjtyYDSK.QX1cDN1wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo "$PWN"
pwn.college{8nGBn2tv50q2mGB608-FjtyYDSK.QX1cDN1wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to store desirable outputs and not just leave them off with the terminal.

## References

None

## Reading Input - Challenge 7
### This challenge requires us to take input of a particular value to a given variable.

**Flag:** `pwn.college{86Fgi5F5L9vxrs_EmtQVtCO3HLa.QX4cTN0wyN4gjNzEzW}` 

The process of obtaining involved:

```
hacker@variables~reading-input:~$ read -p "INPUT: " PWN
INPUT: COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{86Fgi5F5L9vxrs_EmtQVtCO3HLa.QX4cTN0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to take input in the shell to a given variable.

## References

None

## Reading Files - Challenge 8
### This challenge requires us to read the contents of a particular file using a particular command to get the flag.

**Flag:** `pwn.college{Uh4zEzpTjkFm77lNX4cG1xLn7m1.QXwIDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Uh4zEzpTjkFm77lNX4cG1xLn7m1.QXwIDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to read files using the `>` operator.

## References

None


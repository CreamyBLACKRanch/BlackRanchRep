# Digesting Documentation

## Learning From Documentation - Challenge 1
### This challenge requires us to invoke a command followed by an argument correctly to get the flag.

**Flag:** `pwn.college{ov5A_jj6pxg3PtI1L54XJDiSQPJ.QX0ITO0wyN4gjNzEzW}` 

The process of obtaining the flag involved switching to SSH on the pwn.college challenge first, then using the given command along with --giveflag argument.

```
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{ov5A_jj6pxg3PtI1L54XJDiSQPJ.QX0ITO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how a command is executed ONLY with the correct syntax.

## References

None

## Learning Complex uses - Challenge 2
### This challenge requires us to use the --printfile command with the /flag argument.

**Flag:** `pwn.college{8meDqwqaBrVUtOS4Vx15jt6Nip8.QX1ITO0wyN4gjNzEzW}` 

The process of obtaining the flag involved using the /challenge/challenge --printfile /flag command.

```
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{8meDqwqaBrVUtOS4Vx15jt6Nip8.QX1ITO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how usage of few particular commands require rigorous thinking and complex methods.

## References

None

## Reading Manuals - Challenge 3
### This challenge requires us to go through a manual of a commands which will give us the flag.

**Flag:** `pwn.college{8bx_2GF_cD_p4YqiDlx_9YVlMGY.QX0EDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved using man command for challenge and finding the secret command to use to obtain the flag.

```
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge  --bxcpqi 824
Correct usage! Your flag: pwn.college{8bx_2GF_cD_p4YqiDlx_9YVlMGY.QX0EDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how the usage of manuals for a command can be extremely benficial.

## References

None

## Searching Manuals - Challenge 4
### This challenge requires us to go through a manual of a commands which will give us the flag.

**Flag:** `pwn.college{IerAXE_XcjX8QRBqpTS1ifu93E-.QX1EDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved using man command for challenge and finding USING ? or / the secret command to use to obtain the flag.

```
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --rjbxcqc
Initializing...
Correct usage! Your flag: pwn.college{IerAXE_XcjX8QRBqpTS1ifu93E-.QX1EDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how the usage / or ? to find a particular phrase in manuals for a command can be extremely benficial.

## References

None

## Searching For Manuals - Challenge 5
### This challenge requires us to go through a manual of man itself to find the manual thats disguised which will give us the flag.

**Flag:** `pwn.college{4afMGoMRJaGNh8R5tf2sb9XjmZG.QX2EDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved using man of MAN itself to find the afoaht and use ITS manual to get the command to print the flag to obtain the flag.

```
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k /challenge/challenge
afoahtfsbj (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man afoahtfsbj
hacker@man~searching-for-manuals:~$ /challenge/challenge --afoaht 485
Correct usage! Your flag: pwn.college{4afMGoMRJaGNh8R5tf2sb9XjmZG.QX2EDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how the even going through the manual of man itself helps in understanding the complex commands of man.

## References

None

## Helpful Programs - Challenge 6
### This challenge requires us to use the --help to read and get the flag.

**Flag:** `pwn.college{Is4jvzZmMHi2y7568YyKZWw6Wiu.QX3IDO0wyN4gjNzEzW}` 

The process of obtaining the flag the --help command to get the correct value to use as an arg to another command.

```
hacker@man~helpful-programs:~$ /challenge/challenge -h
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 427
hacker@man~helpful-programs:~$ /challenge/challenge -g 427
Correct usage! Your flag: pwn.college{Is4jvzZmMHi2y7568YyKZWw6Wiu.QX3IDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how the usage of --help can be quicker in giving the needed commands over man.

## References

None

## Help For Builtins - Challenge 7
### This challenge requires us to use the help command using the in-built ones in the shell.

**Flag:** `pwn.college{Qm9TrRCZsLtB4y7WbIYRjRQjyH_.QX0ETO0wyN4gjNzEzW}` 

The process of obtaining the flag using the built in help commands for the challenge command and use the secret cmd obtained further for the flag.

```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "Qm9TrRCZ".
hacker@man~help-for-builtins:~$ /challenge --secret Qm9TrRCZ
bash: /challenge: Is a directory
hacker@man~help-for-builtins:~$ challenge --secret Qm9TrRCZ
Correct! Here is your flag!
pwn.college{Qm9TrRCZsLtB4y7WbIYRjRQjyH_.QX0ETO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how the usage of the help functions for BUILT IN commands(in the shell) can help you solve your queries about the command quicker. One mistake I made was using /challenge even when it was a command and not a directory.

## References

None
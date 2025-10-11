# The PATH Variable

## The PATH Variable - Challenge 1
### This challenge demonstrates the importance of the PATH variable and how its absence (export PATH="") prevents basic commands like rm from being found and executed.
**Flag**: `pwn.college{wcjSBBcGZ5aWGDtOYakltBcAVaa.QX2cDM1wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@path~the-path-variable:~$ export PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there!
The flag was revealed afterward:

I might as well give it to you!
pwn.college{wcjSBBcGZ5aWGDtOYakltBcAVaa.QX2cDM1wyN4gjNzEzW}
```

## What I Learned
The challenge taught me that commands executed by the shell must either be specified with their full path (like /challenge/run) or be located in a directory listed in the PATH environment variable. If PATH is empty, standard commands like rm cannot be found or executed.

## References
None

## Setting PATH - Challenge 2
### This challenge requires setting the PATH variable to include the directory containing the necessary win command, allowing the /challenge/run script to find and execute it.
**Flag**: `pwn.college{oxqIDtRD8LLGRDMHkCReX4oZXY6.QX1cjM1wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@path~setting-path:~$ export PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations!
The flag was revealed afterward:

You properly set the flag and 'win' has launched!
pwn.college{oxqIDtRD8LLGRDMHkCReX4oZXY6.QX1cjM1wyN4gjNzEzW}
```
## What I Learned
The challenge taught me how to set the PATH variable using export PATH=... to define which directories the shell should search for executables, enabling successful command execution without specifying the full path.

## References
None

## Finding Commands - Challenge 3
### This challenge requires using the which command to locate the full path of the win executable, which is necessary to find the hidden flag file.
**Flag**: `pwn.college{QQEDX7l05G4rc983bWgFUWWd8eF.01NzEzNxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@path~finding-commands:~$ which win
/challenge/paths/29623/win
hacker@path~finding-commands:~$ cat /challenge/paths/29623/flag
pwn.college{QQEDX7l05G4rc983bWgFUWWd8eF.01NzEzNxwyN4gjNzEzW}
```

## What I Learned
The challenge taught me how to use the which command to quickly determine the full path of an executable that is currently available through the system's PATH. This is a crucial step for discovery in many shell challenges.

## References
None

## Adding Commands - Challenge 4
### This challenge requires creating a local executable, adding its directory to the PATH, and forcing the target script to execute the local version instead of a system one.
**Flag**: `pwn.college{kG-f7rut9xN5MH3gWLhIocdhEj8.QX2cjM1wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@path~adding-commands:~$ which cat
/run/dojo/bin/cat
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ chmod a+x win
hacker@path~adding-commands:~$ PATH=/home/hacker
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{kG-f7rut9xN5MH3gWLhIocdhEj8.QX2cjM1wyN4gjNzEzW}
hacker@path~adding-commands:~$
```

## What I Learned
The challenge taught me how to create and inject a custom command (win) by placing it in a local directory (like /home/hacker), making it executable with chmod a+x, and then setting the PATH to that directory so the system executes the custom script.

## References
None

## Hijacking Commands - Challenge 5
### This challenge requires creating a malicious executable with the same name as a command used by the target script (rm) and placing it earlier in the PATH to hijack the execution.
**Flag**: `pwn.college{gzMvygQXqbO2WWC2yiAso5fagYH.QX3cjM1wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@path~hijacking-commands:~$ which cat
/run/dojo/bin/cat
hacker@path~hijacking-commands:~$ nano rm
hacker@path~hijacking-commands:~$ chmod a+x rm
hacker@path~hijacking-commands:~$ PATH=/home/hacker
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
pwn.college{gzMvygQXqbO2WWC2yiAso5fagYH.QX3cjM1wyN4gjNzEzW}
hacker@path~hijacking-commands:~$
```

## What I Learned
The challenge taught me about command hijacking, where creating a local executable with a common name (like rm), setting its directory at the start of the PATH, and running a script that calls that command will result in the local, custom version being executed instead of the system's official command.

## References
None
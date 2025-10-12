# Processes and Jobs

## Listing Processes - Challenge 1
### This challenge requires us to use the `ps` command to list and find a specific process.

**Flag:** `pwn.college{UzP6htOq13W22dnrEuFJtcAE7fo.QX4MDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@processes~listing-processes:~$ ps ef aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
hacker       137  0.0  0.0 231576  3520 pts/0    Ss   02:31   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-inte
hacker       143  0.0  0.0 231940  4160 pts/0    S    02:31   0:00  _ /run/dojo/bin/bash --login SHELL=/run/dojo/bin/ba
hacker       165  0.0  0.0 233600  3840 pts/0    R+   02:34   0:00      _ ps ef aux SHELL=/run/dojo/bin/bash HOSTNAME=p
root           1  0.0  0.0   1056   640 ? Ss   02:31   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-works
root           7  0.0  0.0 231708  2560 ? S    02:31   0:00 /run/dojo/bin/sleep 6h
root         132  0.0  0.0   4132  2560 ? S    02:31   0:00 /challenge/10935-run-25612
root         135  0.0  0.0   2744  1600 ? S    02:31   0:00  _ sleep 6h
hacker@processes~listing-processes:~$ /challenge/10935-run-25612
Yahaha, you found me!
Here is your flag:
pwn.college{UzP6htOq13W22dnrEuFJtcAE7fo.QX4MDO0wyN4gjNzEzW}
Now I will sleep for a while (so that you could find me with 'ps')
```

## What I Learned

The challenge taught me on how to use the `ps` command with various flags (`ef aux`) to list running processes and find a specific challenge process.

## References

None

## Killing Processes - Challenge 2
### This challenge requires us to use the `kill` command to terminate a running process using its Process ID (PID).

**Flag:** `pwn.college{IGQrxayIfOUllXifc5cBDdeGB6b.QXyQDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@processes~killing-processes:~$ ps -aux -e | grep /challenge/dont_run
hacker       136  0.0  0.0 231576  3520 ? Ss   02:38   0:00 /challenge/dont_run SHELL=/bin/bash HOSTNAME=processes~killing-processes PWD=/home/hacker LOGNAME=hacker _=/challenge/.launcher DOJO_AUTH_TOKEN=f3a799465277dc02b95585119de28a9da619e619db8a1697d33bca9dc265ef97 HOME=/home/hacker USER=hacker SHLVL=0 LC_CTYPE=C.UTF-8 PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin MAIL=/var/mail/hacker DEBIAN_FRONTEND=noninteractive
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job!
Here is your payment:
pwn.college{IGQrxayIfOUllXifc5cBDdeGB6b.QXyQDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to locate a process's PID using `ps` and `grep`, and then use the `kill` command to gracefully terminate it.

## References

None

## Interrupting Processes - Challenge 3
### This challenge requires us to use the keyboard shortcut **Ctrl-C** to interrupt and terminate a running foreground process.

**Flag:** `pwn.college{giBLYt-BODhx1ioIZy_V3GE8izp.QXzQDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job!
You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{giBLYt-BODhx1ioIZy_V3GE8izp.QXzQDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me about the **SIGINT** signal sent by **Ctrl-C** to interrupt a foreground process.

## References

None

## Killing Misbehaving Processes - Challenge 4
### This challenge requires us to identify and kill a specific process to allow the challenge binary to write the flag to a FIFO file.

**Flag:** `pwn.college{YA3SZXIqxQlHZqEnaR-bjgVVpTv.0FNzMDOxwyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@processes~killing-misbehaving-processes:~$ ps -ef -aux | grep /challenge/decoy
hacker       219  0.0  0.0 230696  2560 pts/1    S+   05:05   0:00      _ grep --color=auto /challenge/decoy SHELL=/run/dojo/bin/bash HOSTNAME=processes~killing-misbehaving-processes PWD=/home/hacker MANPATH=/run/dojo/share/man: DOJO_AUTH_TOKEN=2b9649dfb9475875b77625dee84cc9eeb34048393c257d6c240be24f0bd47a94 HOME=/home/hacker LANG=C.UTF-8 TERMINFO=/run/dojo/share/terminfo TERM=xterm-256color SHLVL=2 LC_CTYPE=C.UTF-8 SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin DEBIAN_FRON
hacker@processes~killing-misbehaving-processes:~$ kill 219
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{YA3SZXIqxQlHZqEnaR-bjgVVpTv.0FNzMDOxwyN4gjNzEzW}
```

## What I Learned

The challenge taught me how an interfering process might prevent a program from executing correctly, and how killing it is necessary to proceed.

## References

None

## Suspending Processes - Challenge 5
### This challenge requires us to use the keyboard shortcut **Ctrl-Z** to suspend a running process and then relaunch the program to detect the suspended copy.

**Flag:** `pwn.college{IBTfEYuircHMD8jXFhL2fF48pnL.QX1QDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!
UID          PID    PPID  C STIME TTY          TIME CMD
root         139     129  0 05:08 pts/0    00:00:00 bash /challenge/run
root         141     139  0 05:08 pts/0    00:00:00 ps -f

I don't see a second me!
To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!
UID          PID    PPID  C STIME TTY          TIME CMD
root         139     129  0 05:08 pts/0    00:00:00 bash /challenge/run
root         146     129  0 05:08 pts/0    00:00:00 bash /challenge/run
root         148     146  0 05:08 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{IBTfEYuircHMD8jXFhL2fF48pnL.QX1QDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me about suspending a process using **Ctrl-Z**, which sends the **SIGTSTP** signal, and how it becomes a stopped job in the current shell.

## References

None

## Resuming Processes - Challenge 6
### This challenge requires us to suspend a process and then use the `fg` command to resume it in the foreground.

**Flag:** `pwn.college{0tops35JK3JI-nhLavybvcNfb8E.QX2QDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes!
Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg /challenge/run
/challenge/run
I'm back!
Here's your flag:
pwn.college{0tops35JK3JI-nhLavybvcNfb8E.QX2QDO0wyN4gjNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

## What I Learned

The challenge taught me how to use the `fg` command to bring a stopped or backgrounded job back into the foreground.

## References

None

## Backgrounding Processes - Challenge 7
### This challenge requires us to suspend a process and then use the `bg` command to resume it in the background before launching a new foreground instance.

**Flag:** `pwn.college{U6i_PYcGkDpCBSHuPN9gWBlCypK.QX3QDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running and
not suspended in this terminal... Let's check!
UID          PID STAT CMD
root         138 S+   bash /challenge/run
root         140 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!
To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg /challenge/run
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$

Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.
hacker@processes~backgrounding-processes:~$
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running and
not suspended in this terminal... Let's check!
UID          PID STAT CMD
root         138 S    bash /challenge/run
root         148 S    sleep 6h
root         149 S+   bash /challenge/run
root         151 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background!
Here is the flag:
pwn.college{U6i_PYcGkDpCBSHuPN9gWBlCypK.QX3QDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me how to use the `bg` command to make a stopped job continue execution in the background.

## References

None

## Foregrounding Processes - Challenge 8
### This challenge requires us to move a process from the foreground to the background and back to the foreground (`Ctrl-Z`, `bg`, `fg`).

**Flag:** `pwn.college{QnCKBG0oskU8DpqWWymQNPbPteb.QX4QDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the
background, and then foreground it without re-suspending it! You can
background me with Ctrl-Z (and resume me in the background with 'bg') or, if
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg /challenge/run
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$

Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out. After that, resume me into the foreground with 'fg';
I'll wait.

hacker@processes~foregrounding-processes:~$ fg /challenge/run
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!
pwn.college{QnCKBG0oskU8DpqWWymQNPbPteb.QX4QDO0wyN4gjNzEzW}
```

## What I Learned

The challenge reinforced the use of **Ctrl-Z**, `bg`, and `fg` to manage the state of jobs within a shell session.

## References

None

## Starting backgrounded processes - Challenge 9
### This challenge requires us to use the ampersand symbol (`&`) to start a process directly in the background.

**Flag:** `pwn.college{kTZhpUaNGeJRtvq74ucxKFXOv-_.QX5QDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 138
hacker@processes~starting-backgrounded-processes:~$

Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{kTZhpUaNGeJRtvq74ucxKFXOv-_.QX5QDO0wyN4gjNzEzW}

[1]+  Done                    /challenge/run
```

## What I Learned

The challenge taught me how to use the **`&`** operator to immediately run a command as a background job, freeing up the terminal prompt.

## References

None

## Process Exit Codes - Challenge 10
### This challenge requires us to use the `$?` special variable to read the exit code of the previously executed command.

**Flag:** `pwn.college{4TknXK_JHBv8w1joc3JBzPHIJsR.QX5YDO1wyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo ?183hacker@processes process−exit−codes:  /challenge/submit-code 183
CORRECT! Here is your flag:
pwn.college{4TknXK_JHBv8w1joc3JBzPHIJsR.QX5YDO1wyN4gjNzEzW}
```

## What I Learned

The challenge taught me about **process exit codes** and how the special variable **`$?`** holds the exit status of the most recently executed foreground command.

## References

None
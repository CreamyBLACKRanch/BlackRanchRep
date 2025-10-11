# Terminal Multiplexing (Screen and Tmux)

## Launching Screen - Challenge 1
### This challenge requires us to start a new terminal multiplexer session using the `screen` command.

**Flag:** `pwn.college{IO2oTD8-URrPyX6QvJfLHcQEk6u.0VN4IDOxwyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
Congratulations! You're inside a screen session!
Here's your flag:
pwn.college{IO2oTD8-URrPyX6QvJfLHcQEk6u.0VN4IDOxwyN4gjNzEzW}
```
## What I Learned
The challenge taught me the basic command for initiating a screen session, which allows for multiple persistent terminal windows within a single shell.

## References
None

## Detaching and Attaching - Challenge 2
### This challenge requires us to detach from a running screen session (using Ctrl+A,D) and then re-attach to it later (using screen -r).
**Flag**: `pwn.college{kNYp9s-h6BPXHOB1Kbs783JmVAm.0lN4IDOxwyN4gjNzEzW}`

```
The process of obtaining the flag involved:

hacker@terminal-multiplexing~detaching-and-attaching:~$
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{kNYp9s-h6BPXHOB1Kbs783JmVAm.0lN4IDOxwyN4gjNzEzW}
Yes! Flag is: pwn.college{kNYp9s-h6BPXHOB1Kbs783JmVAm.0lN4IDOxwyN4gjNzEzW}
```

## What I Learned
The challenge taught me the keyboard shortcut (Ctrl+A,D) and the command (screen -r) necessary to detach from and re-attach to a screen session, keeping processes running in the background.

## References
None

## Finding Sessions - Challenge 3
### This challenge requires us to list all active screen sessions using the screen -ls command to identify a specific, named session.
**Flag**: `pwn.college{oUBcIqTKDjcsxoxhdYC3Y3A_X79.01N4IDOxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{oUBcIqTKDjcsxoxhdYC3Y3A_X79.01N4IDOxwyN4gjNzEzW}
pwn.college{oUBcIqTKDjcsxoxhdYC3Y3A_X79.01N4IDOxwyN4gjNzEzW}
```

## What I Learned
The challenge taught me how to use the screen -ls command to view a list of all currently running and attachable screen sessions.

## References
None

## Switching Windows - Challenge 4
### This challenge requires us to switch between windows within a screen session using the key sequences Ctrl+A,1 and Ctrl+A,0.
**Flag**: `pwn.college{kz0zoT7z2CBgExsK9qbwjsE_-gV.0FO4IDOxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
The process of obtaining the flag involved:
hacker@terminal-multiplexing~switching-windows:~$ screen -r
ctrl + A 1
ctrl + A 0
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work!
You found window 0!
> Here is your flag: pwn.college{kz0zoT7z2CBgExsK9qbwjsE_-gV.0FO4IDOxwyN4gjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{kz0zoT7z2CBgExsK9qbwjsE_-gV.0FO4IDOxwyN4gjNzEzW}
```
## What I Learned
The challenge taught me the keybinds (Ctrl+A,n) for switching to a specific window number within a running screen session.

## References
None

## Detaching and Attatching (tmux) - Challenge 5
### This challenge requires us to detach from a running tmux session (using Ctrl+B,D) and then re-attach to it later (using tmux attach).
**Flag**: `pwn.college{AefevrpouVcErX6bZ1bDSr-pdxC.0VO4IDOxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{AefevrpouVcErX6bZ1bDSr-pdxC.0VO4IDOxwyN4gjNzEzW}
Congratulations, here is your flag: pwn.college{AefevrpouVcErX6bZ1bDSr-pdxC.0VO4IDOxwyN4gjNzEzW}
```

## What I Learned
The challenge taught me the process of detaching and re-attaching to a tmux session, using its specific prefix (Ctrl+B) followed by the detach command (D) and then tmux attach.

## References
None

## Switching Windows (tmux) - Challenge 6
### This challenge requires us to switch between windows within a tmux session using the key sequences Ctrl+B,1 and Ctrl+B,0.
**Flag**: `pwn.college{Umv-8q_ip-KNj29G-HpdJf9T9WE.0FM5IDOxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Excellent work!
You found window 0!
> Here is your flag: pwn.college{Umv-8q_ip-KNj29G-HpdJf9T9WE.0FM5IDOxwyN4gjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{Umv-8q_ip-KNj29G-HpdJf9T9WE.0FM5IDOxwyN4gjNzEzW}
hacker@terminal-multiplexing~switching-windows-tmux:~$
```

## What I Learned
The challenge taught me the tmux specific keybinds (Ctrl+B prefix) for switching between different windows based on their numerical index.

## References
None
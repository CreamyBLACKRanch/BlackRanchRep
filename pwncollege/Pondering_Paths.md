# Pondering Paths

## The Root - Challenge 1
### This challenge requires us to invoke the / command followed by a directory to get the flag.

**Flag:** `pwn.college{UCuEHzvai4kdcjRGXah61c7hMzY.QX4cTO0wyN4gjNzEzW}` 

The process of obtaining the flag involved switching to SSH on the pwn.college challenge first, then using the / followed by 'pwn' to move into the directory of /pwn to get the flag.

```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{UCuEHzvai4kdcjRGXah61c7hMzY.QX4cTO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to navigate through sub directories using the main i.e the / command.

## References

None

## Programs and absolute paths - Challenge 2
### This challenge requires us to navigate to the challenge directory for 'run' which gives us the flag.

**Flag:** `pwn.college{M1ZXHsyaSSyjtxGe56NYblOf3Of.QX1QTN0wyN4gjNzEzW}` 

The process of obtaining the flag involved navigating to the /challenge/run directory i.e the absolute path.

```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{M1ZXHsyaSSyjtxGe56NYblOf3Of.QX1QTN0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to access a file or directory using direct path. One initial mistake I made was using 'cd' before /challenge/run, then realised it wasn't needed.

## References

None

## Position Thy Self - Challenge 3
### This challenge requires us to navigate to the challenge directory using the 'change directory(cd)' command which gives us the flag.

**Flag:** `pwn.college{QgDYBM79bx2G6ux622s01M9sMpl.QX2QTN0wyN4gjNzEzW}` 

The process of obtaining the flag involved navigating to the /challenge/run first, which gave us the directory to actually go to using the cd command to get the flag.

```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/zoneinfo/posix/Asia directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /usr/share/zoneinfo/posix/Asia
hacker@paths~position-thy-self:/usr/share/zoneinfo/posix/Asia$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{QgDYBM79bx2G6ux622s01M9sMpl.QX2QTN0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to access a file or directory using the cd command. It helped me navigate to a directory before executing /challenge/run. My mistake was using the cd command directly without running /challenge/hacker first to obtain the directory to 'cd' into.

## References

None

## Position Elsewhere - Challenge 4
### This challenge requires us to navigate to the usr/include directory using the 'change directory(cd)' command which gives us the flag.

**Flag:** `pwn.college{EmLPQKYaCMEc9KgfmqBWMGl0YJe.QX3QTN0wyN4gjNzEzW}` 

The process of obtaining the flag involved navigating to the /challenge/run first, which gave us the directory to actually go to using the cd command to get the flag.

```
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/include directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/include
hacker@paths~position-elsewhere:/usr/include$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{EmLPQKYaCMEc9KgfmqBWMGl0YJe.QX3QTN0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to access a file or directory using the cd command. It helped me understand as to how to use an absolute path right from the directory we changed to.

## References

None

## Position Yet Elsewhere - Challenge 5
### This challenge requires us to navigate to the /proc/131/fd directory using the 'change directory(cd)' command which gives us the flag.

**Flag:** `pwn.college{Q3SNB4I4Xi2m4ClBCnNtJ9f43NC.QX4QTN0wyN4gjNzEzW}` 

The process of obtaining the flag involved navigating to the /challenge/run first, which gave us the directory to actually go to using the cd command to get the flag.

```
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /proc/131/fd directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /proc/131/fd
hacker@paths~position-yet-elsewhere:/proc/131/fd$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Q3SNB4I4Xi2m4ClBCnNtJ9f43NC.QX4QTN0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to access a file or directory using the cd command. It helped me understand as to how to use an absolute path right from the directory we changed to.

## References

None

## Implicit Relative Paths, from / - Challenge 6
### This challenge requires us to navigate to the / directory using the 'change directory(cd)' and then run the relative path to obtain the flag.

**Flag:** `pwn.college{opMxHR2rgiJwZK-DTbn4uXy9x0h.QX5QTN0wyN4gjNzEzW}` 

The process of obtaining the flag involved navigating to the /directory using cd first, and then running the challenge/run relative path.

```
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{opMxHR2rgiJwZK-DTbn4uXy9x0h.QX5QTN0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to access a file or directory directly using relative paths when the target is already in your current working directory.

## References

None

## Explicit Relative Paths, from / - Challenge 7
### This challenge requires us to navigate to the / directory using the 'change directory(cd)' and then use explicit relative paths to get the flag.

**Flag:** `pwn.college{4sRWLAHk0fO7LqjTGZ3Xv1p2wKm.QXwUTN0wyN4gjNzEzW}` 

The process of obtaining the flag involved navigating to the /directory using cd first, using explicit relative paths, in this case './challenge/run'.

```
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{4sRWLAHk0fO7LqjTGZ3Xv1p2wKm.QXwUTN0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to access a file or directory directly using explicit relative paths when the target is already in your current working directory.

## References

None

## Implicit Relative Paths - Challenge 8    
### This challenge requires us to navigate to the /challenge directory using the 'change directory(cd)' and then use  relative paths to get the flag.

**Flag:** `pwn.college{QxRD4qr8LP9o37TUnUc4XvOEJxJ.QXxUTN0wyN4gjNzEzW}` 

The process of obtaining the flag involved navigating to the /challenge directory using cd first, using relative paths, in this case './run'.

```
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{QxRD4qr8LP9o37TUnUc4XvOEJxJ.QXxUTN0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how linux doesn't run a program when provided a naked 'absolute path' as a safety measure and needs an ./ implicit path inside the cwd to run it.

## References

None

## Home Sweet Home - Challenge 9   
### This challenge requires us to provide an absolute path and file along with /challenge/run which write the flag and reads it to us.

**Flag:** `pwn.college{oyLnFMt0xR5S9H-NqghmvBk8yiS.QXzMDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved providing an absolute path of a file for the flag to be written into.

```
hacker@paths~home-sweet-home:~$ /challenge/run ~/trr
The argument you provided must not have been longer than 3 characters (it's
currently 5 characters long)!
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{oyLnFMt0xR5S9H-NqghmvBk8yiS.QXzMDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how linux always considers ~ as the home directory and how it expands into it when asked to using ~.

## References

None
# File Globbing

## Matching with * - Challenge 1
### This challenge requires us to use the * to match the directory to cd into.

**Flag:** `pwn.college{ENqtCqivGmwQIhR-2zviUOLPEtN.QXxIDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved switching to SSH on the pwn.college challenge first, then using the given command along the * (matching operator).

```
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{ENqtCqivGmwQIhR-2zviUOLPEtN.QXxIDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to use the matching operator.

## References

None

## Matching with ? - Challenge 2
### This challenge requires us to use the ? as a matching operator.

**Flag:** `pwn.college{4l6bjAtIzfmglKBWhJPU-gvLTPs.QXyIDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved using the ? match operator to get into the working directory.

```
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /?????enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{4l6bjAtIzfmglKBWhJPU-gvLTPs.QXyIDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to use the match operator with ?.

## References

None

## Matching with [] - Challenge 3
### This challenge requires us to use the [] matching operator to find the flag.

**Flag:** `pwn.college{cxP42buo9-EZoE8t-p8eYiwJ51K.QXzIDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved using the match operator using [].

```
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{cxP42buo9-EZoE8t-p8eYiwJ51K.QXzIDO0wyN4gjNzEzW}
hacker@globbing~matching-with-:/challenge/files$
```

## What I Learned

The challenge taught me on how the usage of the [] along with match operator.

## References

None

## Matching Paths with [] - Challenge 4
### This challenge requires us to use the [] matching operator along with the path to get the flag.

**Flag:** `pwn.college{ELNkdybzxnryc-kAjB-8vlY1ifo.QX0IDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved using the [] match operator along with path of the file to run.

```
Connected!
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{ELNkdybzxnryc-kAjB-8vlY1ifo.QX0IDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how the usage of [] along with the path makes it easier to run files from home directory.

## References

None

## Multiple Globs - Challenge 5
### This challenge requires us to use multiple globs to find the flag in one of many files that are similarly titled.

**Flag:** `pwn.college{cnp3tHdV-GWOk-Gig5OCiKiQAm9.0lM3kjNxwyN4gjNzEzW}` 

The process of obtaining the flag involved using multiple glob i.e *p* to find the flag.

```
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{cnp3tHdV-GWOk-Gig5OCiKiQAm9.0lM3kjNxwyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how using the multiple glob command helps go through many files that are similar with minimal arguments.

## References

None

## Mixing Globs - Challenge 6
### This challenge requires us to use mixed globs to obtain the flag in a file.

**Flag:** `pwn.college{EOwTxN0v-oTL0rXn6JEHe3Fp_26.QX1IDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved using the mixed glob []* to get the flag.

```
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run *[cp]*
Your expansion did not expand to the requested files (challenging, educational,
pwning). Instead, it expanded to:
challenging educational fantastic happy incredible magical nice optimistic pwning splendid uplifting victorious
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cpe]*
You got it! Here is your flag!
pwn.college{EOwTxN0v-oTL0rXn6JEHe3Fp_26.QX1IDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how the usage of mixed globs to run particualr files that match the particular criteria.

## References

None

## Exclusion Globs - Challenge 7
### This challenge requires us to use excluded command to obtain flags in a file without the words p,w,n.

**Flag:** `pwn.college{0k2nAbwl955oiFHuZ_WvlUwfWDY.QX2IDO0wyN4gjNzEzW}` 

The process of obtaining the flag using exclusion glob command to obtain the flag.

```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files/
hacker@globbing~exclusionary-globbing:/challenge/files$ ls
amazing    challenging  educational  great  incredible  kind      magical  optimistic  queenly  splendid   uplifting   wonderful  youthful
beautiful  delightful   fantastic    happy  jovial      laughing  nice     pwning      radiant  thrilling  victorious  xenial     zesty
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{0k2nAbwl955oiFHuZ_WvlUwfWDY.QX2IDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how the usage of exclusion glob helps find a targetted group of files easily.

## References

None

## Tab Completion - Challenge 8
### This challenge requires us to use tab to complete commands for the suggested ones by the terminal.

**Flag:** `pwn.college{0qMexEJVkgJ-5KtC2dmoDfB3oN9.0FN0EzNxwyN4gjNzEzW}` 

The process of obtaining the flag using the tab completion to access a file in a given directory.

```
hacker@globbing~tab-completion:~$ ccat /challenge/pwncollege​
.bash_history  .config/       .lesshst       a              b              not-the-flag
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​ not-the-flag
pwn.college{0qMexEJVkgJ-5KtC2dmoDfB3oN9.0FN0EzNxwyN4gjNzEzW}
cat: not-the-flag: Permission denied
```

## What I Learned

The challenge taught me on how to use the tab to complete the commands to get through them easier.

## References

None

## Multiple options for Tab Completion - Challenge 9
### This challenge requires us to use tab to complete commands for the suggested ones by the terminal.

**Flag:** `pwn.college{0WJr2lasooR29uLgkFNw3wBnuzn.0lN0EzNxwyN4gjNzEzW}` 

The process of obtaining the flag using the tab completion to access a file in a given directory.

```
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/
hack-the-planet        pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-fl
pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
```

## What I Learned

The challenge taught me on how to use the tab to complete the commands to get through them easier.

## References

None

## Tab Completion On Commands - Challenge 10
### This challenge requires us to use tab to complete commands for the suggested ones by the terminal.

**Flag:** `pwn.college{02UQrzcZFWS3BfzT8zsILBLFYPh.0VN0EzNxwyN4gjNzEzW}` 

The process of obtaining the flag using the tab completion to access a file in a given directory.

```
Connected!
hacker@globbing~tab-completion-on-commands:~$ pwncollege-21943
Correct! Here is your flag:
pwn.college{02UQrzcZFWS3BfzT8zsILBLFYPh.0VN0EzNxwyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to use the tab to complete even for commands to make them easier.

## References

None
# Practicing Piping

## Redirecting Output - 1
### This challenge requires us to redirect output to a file using `>`.

**Flag:** `pwn.college{AD6QH9kJkiOPnioQzhrRbLR7SqV.QX0YTN0wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{AD6QH9kJkiOPnioQzhrRbLR7SqV.QX0YTN0wyN4gjNzEzW}
```
 
## What I Learned

How to redirect standard output to a file using `>`.

## References

None


## Redirecting More Output - 2
### This challenge involves redirecting output of a command into a file and retrieving a flag from it.

**Flag:** `pwn.college{U-3qVedpig7sYqrQ6Ic-yOfrFQl.QX1YTN0wyN4gjNzEzW}`

```
The process of obtaining the flag involved:

hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
...
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{U-3qVedpig7sYqrQ6Ic-yOfrFQl.QX1YTN0wyN4gjNzEzW}
```

## What I Learned

How to capture program output into a file and view it later.

## References

None


## Appending Output - 3
### This challenge checks if output was appended correctly using `>>`.

**Flag:** `pwn.college{QA1k2DmhrnUUCNrv9bl4h8sSSeE.QX3ATO0wyN4gjNzEzW}`

```
The process of obtaining the flag involved:

hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
...
hacker@piping~appending-output:~$ cat the-flag
|
|/ This is the first half:
v
pwn.college{QA1k2DmhrnUUCNrv9bl4h8sSSeE.QX3ATO0wyN4gjNzEzW}
```
 

## What I Learned

How to append output using `>>` without overwriting existing file content.

## References

None
 
## Redirecting Errors - 4
### This challenge requires redirecting error output (`stderr`) using `2>`.

**Flag:** `pwn.college{ErU_aliBu0_8aLmUQxYIJ9agnwC.QX3YTN0wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{ErU_aliBu0_8aLmUQxYIJ9agnwC.QX3YTN0wyN4gjNzEzW}
```

## What I Learned

How to redirect standard error separately from standard output.

## References

None
 

## Redirecting Input - 5
### This challenge involves redirecting input into a program using `<`.

**Flag:** `pwn.college{8I2zTUzz7Fu82dalXTq341BHBTm.QXwcTN0wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
...
Here is your flag:
pwn.college{8I2zTUzz7Fu82dalXTq341BHBTm.QXwcTN0wyN4gjNzEzW}
```

## What I Learned

How to use `<` to feed a file's contents into a program.

## References

None
 

## Grepping Stored results - 6
### This challenge involves grepping a saved file to extract the flag.

**Flag:** `pwn.college{AoN6_PqlmcLj_Eu2r-zMM5yX1Js.QX4EDO0wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
...
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
pwn.college{AoN6_PqlmcLj_Eu2r-zMM5yX1Js.QX4EDO0wyN4gjNzEzW}
```

## What I Learned

How to redirect output and search within it using `grep`.

## References

None
 

## Grepping Live output - 7
### This challenge involves piping live output directly into `grep`.

**Flag:** `pwn.college{AK9XwtUxlotqKhQyfqT27qg_MLD.QX5EDO0wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
...
pwn.college{AK9XwtUxlotqKhQyfqT27qg_MLD.QX5EDO0wyN4gjNzEzW}
```
 
## What I Learned

How to use pipes (`|`) to process live output with another program like `grep`.

## References

None

## Grepping Errors - 8(Redo)
### This challenge involves piping errors directly into `grep`.

**Flag:** `pwn.college{AK9XwtUxlotqKhQyfqT27qg_MLD.QX5EDO0wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
...
pwn.college{AK9XwtUxlotqKhQyfqT27qg_MLD.QX5EDO0wyN4gjNzEzW}
``` 
 
## What I Learned

How to use pipes (`|`) to process live output with another program like `grep`.

## References

None

## Filtering with Grep -v - 9
### This challenge involves piping the flag directly using  `grep` and -v.

**Flag:** `pwn.college{Ql4rmIe1BE3OA-R6mwNh_Tjp6d2.0FOxEzNxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{Ql4rmIe1BE3OA-R6mwNh_Tjp6d2.0FOxEzNxwyN4gjNzEzW}
```
 
## What I Learned

How to use the `grep` with the filter `-v` command.

## References

None

## Duplicating Piped Date with tee - 10(Redo)
### This challenge involves piping the flag using the `tee` command.

**Flag:** `pwn.college{Ql4rmIe1BE3OA-R6mwNh_Tjp6d2.0FOxEzNxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{Ql4rmIe1BE3OA-R6mwNh_Tjp6d2.0FOxEzNxwyN4gjNzEzW}
```
 
## What I Learned

How to use the `grep` with the filter `-v` command.

## References

None

## Process Substitution For Input - 11
### This challenge involves piping the flag and using the diff operator to get the flag.

**Flag:** ` pwn.college{4AmJCWQd4oQ71AeC-mtSiCPdVMb.0lNwMDOxwyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
58a59
> pwn.college{4AmJCWQd4oQ71AeC-mtSiCPdVMb.0lNwMDOxwyN4gjNzEzW}
```
 
## What I Learned

How to use the `diff` operator to find differences easily between to components. I also learned about how a temporary file is created with the output to be read by the diff operator.

## References

None

## Writing to multiple programs - 12
### This challenge involves on learning process sub also WRITE commands.

**Flag:** `pwn.college{Q8pRnUTX34L3TQzBlmnP4DRJ4sf.QXwgDN1wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >( /challenge/the ) | /challenge/planet
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{Q8pRnUTX34L3TQzBlmnP4DRJ4sf.QXwgDN1wyN4gjNzEzW}
```
 
## What I Learned

How to use the Process Substitution command for writing commands and also showed how it is a special tool with a wide vareity of uses.

## References

None

## Split Piping Stderr and Stdout - 13
### This challenge involves using the stderr and stdout commands WITHOUT mixing them to obtain the proper flag.

**Flag:** `pwn.college{QPgncQILjiDf3sNx3zQ6cTX6bia.QXxQDM2wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >( /challenge/planet ) 2> >( /challenge/the )
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{QPgncQILjiDf3sNx3zQ6cTX6bia.QXxQDM2wyN4gjNzEzW}
```
 
## What I Learned

How to use the piping commands of stdin and stdout properly without mixing them. I initially kept making the mistake of ignoring the second `>` after /hack which took me long to get over.

## References

None

## Named Pipes - 14(Redo)
### This challenge involves using the stderr and stdout commands WITHOUT mixing them to obtain the proper flag.

**Flag:** `pwn.college{QPgncQILjiDf3sNx3zQ6cTX6bia.QXxQDM2wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >( /challenge/planet ) 2> >( /challenge/the )
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{QPgncQILjiDf3sNx3zQ6cTX6bia.QXxQDM2wyN4gjNzEzW}
```
 
## What I Learned

How to use the piping commands of stdin and stdout properly without mixing them. I initially kept making the mistake of ignoring the second `>` after /hack which took me long to get over.

## References

None
# Data Manipulation

## Translating Characters - Challenge 1
### This challenge requires us to use the `tr` command to translate characters by case-swapping.

**Flag:** `pwn.college{kv-TKHxkk8hhY3k5zobH5jq9YnH.01MxEzNxwyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@data~translating-characters:~$ /challenge/run | tr 'A-Za-z' 'a-zA-Z'
yOUR CASE-SWAPPED FLAG:
pwn.college{kv-TKHxkk8hhY3k5zobH5jq9YnH.01MxEzNxwyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to use the `tr` command with character sets to perform case translation (swapping upper and lower case).

## References

None

## Deleting Characters - Challenge 2
### This challenge requires us to use the `tr` command with the delete flag (`-d`) to remove specific unwanted characters.

**Flag:** `pwn.college{s1nQTdy6CGSfBS7PPrAPigL7D6Q.0FNxEzNxwyN4gjNzEzW}` 

```
The process of obtaining the flag involved:

hacker@data~deleting-characters:~$ /challenge/run | tr -d %^
Your character-stuffed flag:
pwn.college{s1nQTdy6CGSfBS7PPrAPigL7D6Q.0FNxEzNxwyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to use `tr -d` to remove specific characters (`%` and `^`) from a stream of text.

## References

None

## Deleting Newlines - Challenge 3
### This challenge requires us to use the `tr` command to delete newline characters (`\n`) to get the flag on a single line.

**Flag:** `pwn.college{AxepXxUzrVeIabcWb3CkHRvlBv6.0VNxEzNxwyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{AxepXxUzrVeIabcWb3CkHRvlBv6.0VNxEzNxwyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to use `tr -d "\n"` to strip newline characters and join split text into a single line.

## References

None

## Extracting the First Lines with Head - Challenge 4
### This challenge requires us to use the `head` command to extract a specific number of lines from the output.

**Flag:** `pwn.college{EDHyRsTznShgR7VDvMHgaGVelbW.0lNxEzNxwyN4gjNzEzW}` 

```
The process of obtaining the flag involved:
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{EDHyRsTznShgR7VDvMHgaGVelbW.0lNxEzNxwyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to use `head -n X` to pipe only the first `X` lines of output to a subsequent command.

## References

None

## Extracting Specific Sections of a Text - Challenge 5
### This challenge requires us to use the `cut` command to extract a specific field (section) from the output and then remove the newline character.

**Flag:** `pwn.college{IcEWUvqprgpAI0OqlI6KsFZ7xAa.01NxEzNxwyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{IcEWUvqprgpAI0OqlI6KsFZ7xAa.01NxEzNxwyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to use `cut` with the delimiter flag (`-d`) and field flag (`-f`) to isolate a specific column of data.

## References

None

## Sorting Data - Challenge 6
### This challenge requires us to use the `sort` command with the reverse flag (`-r`) to sort the data in descending order.

**Flag:** `pwn.college{AaPzAe34ehcgval9ohTCQOEmKAi.0FM0MDOxwyN4gjNzEzW}` 

The process of obtaining the flag involved:

```
hacker@data~sorting-data:~$ sort /challenge/flags.txt -r
pwn.college{AaPzAe34ehcgval9ohTCQOEmKAi.0FM0MDOxwyN4gjNzEzW}
pwn.college{AaPzAe34ehcgval9ohTCQOEmKAi.0FM0MDOxwyN4gjNyEzW}
pwn.college{AaPzAe34ehcgval9ohTCQOEmKAi.0FM0MDOxwxM4gjNzEzW}
pwn.college{AaPzAe34ehcgval9ohTCQOEmKAi.0FM0MDOxvyN4gjMzEzW}
pwn.college{AaPzAe34ehcgval9ohTCQOEmKAh.0FM0MDOwwyN4gjNzEzW}
pwn.college{AaPzAe34ehcgval9ohSCQOEmKAh.0FM0MCOwwyN4gjNzEzW}
pwn.college{AaPzAe34ehcgval9ogSCQODmKAi.0FM0MDOxwyM4gjNzEzW}
pwn.college{AaPzAe34dhcgval9ohTBQOEmKAi.0EM0MDOxvyN4gjMzEzW}
pwn.college{AaPzAe33ehbgvak8nhSBPNElJAi.0FL0MDOxvyN3giMzEyW}
pwn.college{AaPzAe33dgcgval9ohTCQODmKAi.0FM0MCOxwyN3gjNzEzV}
pwn.college{AaPzAe24ehcfual9nhTCPOEmKAi.0FM0MDNwvyN3gjNzDzW}
pwn.college{AaPzAe24ehbgvak9ohTBQOEmKAi.0FM0MDOxvyN4gjNzDzW}
pwn.college{AaPzAe24egcfval9ohTCQOElJAi.0EM0MDNxwyN4gjNzEzW}
pwn.college{AaPzAe23ehcgvak9ogSBQOEmKAh.0EM0MCNxwyN4giMzEzV}.....(and many more)
```

## What I Learned

The challenge taught me on how to use the `sort` command to order lines of text and how to use the `-r` flag for reverse (descending) sorting.

## References

None
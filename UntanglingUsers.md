# Untangling Users

## Becoming root with su - Challenge 1
### This challenge requires us to use the `su` command to switch to the **root** user.

**Flag:** `pwn.college{Enm3G9vNw6_jBAhPkzEgRUGqIfs.QX1UDN1wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
creamyranch@LAPTOP-0P5A2GVI:~$ ssh -i key hacker@dojo.pwn.college
Connected!
hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{Enm3G9vNw6_jBAhPkzEgRUGqIfs.QX1UDN1wyN4gjNzEzW}
```

## What I Learned

The challenge taught me how to use the **`su`** command without a specified username to switch to the **root** user, and then read the flag.

## References

None

---

## others with su - Challenge 2
### This challenge requires us to use the `su` command to switch to a **different, non-root user** named `zardus`.

**Flag:** `pwn.college{gPm3B1Rs8eVw2HOrmvyLkwb6Bpq.QX2UDN1wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus!
Here is your flag:
pwn.college{gPm3B1Rs8eVw2HOrmvyLkwb6Bpq.QX2UDN1wyN4gjNzEzW}
```

## What I Learned

The challenge reinforced the use of **`su`** with a username argument (e.g., `su zardus`) to switch to a specific, non-root account.

## References

None

---

## Cracking Passwords - Challenge 3
### This challenge requires us to use the password cracking tool **John the Ripper** (`john`) to find a user's password and then use the `su` command to switch to that user.

**Flag:** `pwn.college{E_J3iaHZt7Mw9RY6PtlVBxcT2R6.QX3UDN1wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
0g 0:00:00:01 28% 1/3 0g/s 289.4p/s 289.4c/s 289.4C/s sudraz!..bzardus
0g 0:00:00:03 37% 1/3 0g/s 286.0p/s 286.0c/s 286.0C/s Ozardus99999...zardus
0g 0:00:00:04 54% 1/3 0g/s 287.2p/s 287.2c/s 287.2C/s zrdus..zardus9999994
0g 0:00:00:06 69% 1/3 0g/s 287.5p/s 287.5c/s 287.5C/s Z99999E..1z999991
0g 0:00:00:07 76% 1/3 0g/s 288.0p/s 288.0c/s 288.0C/s 9999945..Z9999932
0g 0:00:00:08 85% 1/3 0g/s 288.0p/s 288.0c/s 288.0C/s Zardus1111..z99999123456
0g 0:00:00:09 93% 1/3 0g/s 286.0p/s 286.0c/s 286.0C/s zardus999992002..zardus1963
0g 0:00:00:10 99% 1/3 0g/s 286.2p/s 286.2c/s 286.2C/s zardus999991915..999991900
0g 0:00:00:12 0% 2/3 0g/s 286.5p/s 286.5c/s 286.5C/s kelly..snickers
0g 0:00:00:14 0% 2/3
0g/s 286.7p/s 286.7c/s 286.7C/s Alexis..bigred
0g 0:00:00:16 0% 2/3 0g/s 287.2p/s 287.2c/s 287.2C/s rockie..surfing
0g 0:00:00:18 1% 2/3 0g/s 287.3p/s 287.3c/s 287.3C/s chacha..jazmin
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04935g/s 287.4p/s 287.4c/s 287.4C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus!
Here is your flag:
pwn.college{E_J3iaHZt7Mw9RY6PtlVBxcT2R6.QX3UDN1wyN4gjNzEzW}
```

## What I Learned

The challenge demonstrated using **John the Ripper** to crack a leaked password hash, revealing the password (`aardvark`), and then applying it to successfully switch users with **`su`**.

## References

None

---

## Using Sudo - Challenge 4
### This challenge requires us to use the `sudo` command to execute a command with **root privileges** without explicitly switching users.

**Flag:** `pwn.college{cBAaAo13Fwq9YsQ0j7ig7NTHWR0.QX4UDN1wyN4gjNzEzW}`

The process of obtaining the flag involved:

```
hacker@users~using-sudo:~$ cat /flag
cat: /flag: Permission denied
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{cBAaAo13Fwq9YsQ0j7ig7NTHWR0.QX4UDN1wyN4gjNzEzW}
```

## What I Learned

The challenge taught me how to use the **`sudo`** command to temporarily gain elevated privileges for a single command, which is often used instead of a full user switch with `su`.

## References

None
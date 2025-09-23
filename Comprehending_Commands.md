# Comprehending Commands

## Cat - not the pet, but the command! - Challenge 1
### This challenge requires us to invoke the cat command follwed by the file name to get the flag.

**Flag:** `pwn.college{o5J7X2K5frSVC0FEu8PxuGvoXSY.QXxcTN0wyN4gjNzEzW}` 

The process of obtaining the flag involved switching to SSH on the pwn.college challenge first, then using the cat command along with the flag file to get the flag.

```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{o5J7X2K5frSVC0FEu8PxuGvoXSY.QXxcTN0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how the cat command works and its functionality.

## References

None

## Catting absolute paths - Challenge 2
### This challenge requires us to use the cat command for the absolute path of a file which gives us the flag.

**Flag:** `pwn.college{EzaSaHatcQq3V_T4CwKc7Om135_.QX5ETO0wyN4gjNzEzW}` 

The process of obtaining the flag involved using the cat commands followed by the absolute path of the flag file.

```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{EzaSaHatcQq3V_T4CwKc7Om135_.QX5ETO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to read a file using the cat command with the absolute path of the file.

## References

None

## More catting practice - Challenge 3
### This challenge requires us to use the cat command along with the absolute path of a hidden file.

**Flag:** `pwn.college{ElifP-radE5YjL4EeoBTCyPwQ-b.QXwITO0wyN4gjNzEzW}` 

The process of obtaining the flag involved using cd, which gave us the directory and the catting the absolute path of the file.

```
hacker@commands~more-catting-practice:~$ cd
You used 'cd'! In this level, I don't allow you to change the working directory
--- you MUST chase pass 'cat' the absolute path of where I put it on the
filesystem (which is /usr/share/nodejs/flag).
hacker@commands~more-catting-practice:~$ cat /usr/share/nodejs/flag
pwn.college{ElifP-radE5YjL4EeoBTCyPwQ-b.QXwITO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to read a file using the cat command with the absolute path of the file..

## References

None

## Grepping for a needle in a haystack - Challenge 4
### This challenge requires us to use the grep command to find the flag.

**Flag:** `pwn.college{M8a2hGNzGHn368NJ4m1fMEiDoIF.QX3EDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved using the grep commands followed by the required substring to be found in a large text file.

```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{M8a2hGNzGHn368NJ4m1fMEiDoIF.QX3EDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to access a large file that can't be read by cat, but can be read by grep to find a specific keyword too.

## References

None

## Comparing Files - Challenge 5
### This challenge requires us to use the diff command to find the real flag in two files.

**Flag:** `pwn.college{YZLL_QYXDBMGEybs8tY3KZmNPCb.01MwMDOxwyN4gjNzEzW}` 

The process of obtaining the flag involved using the diff f1 f2 command to find the only real flag by comparing the two files.

```
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
97a98
> pwn.college{YZLL_QYXDBMGEybs8tY3KZmNPCb.01MwMDOxwyN4gjNzEzW}
```

## What I Learned

The challenge taught me how the diff command works and can be used to find differences among larger files very easily.

## References

None

## Listing Files - Challenge 6
### This challenge requires us to list the files in a given directory to obtain the flag.

**Flag:** `pwn.college{kBzNvJKyqTBpoiPC4krHDFz5PVz.QX4IDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved listing files in the challenge directory and then executing a file in it.

```
hacker@commands~listing-files:~$ ls /challenge
10697-renamed-run-27871  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/10697-renamed-run-27871
Yahaha, you found me! Here is your flag:
pwn.college{kBzNvJKyqTBpoiPC4krHDFz5PVz.QX4IDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to access a file or directory after finding it using the list command.

## References

None

## Touching Files - Challenge 7
### This challenge requires us to create two files in the specified directories to get the flag.

**Flag:** `pwn.college{kK4GQoMgpEQesbl_IRepIquOLSN.QXwMDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved navigating to the /tmp directory using cd first, then using the touch command to create two files pwn and college to get the flag'.

```
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{kK4GQoMgpEQesbl_IRepIquOLSN.QXwMDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to create a file in a specified directory using the touch command.

## References

None

## Removing files - Challenge 8    
### This challenge requires us to remove a file and then check it to get the flag.

**Flag:** `pwn.college{UzvRh__uYN3qn1WmxxRhq2Wqf3Q.QX2kDM1wyN4gjNzEzW}` 

The process of obtaining the flag involved checking the contents of the home directory and then using the rm command to delete the file.

```
hacker@commands~removing-files:~$ ls
a  b  delete_me
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{UzvRh__uYN3qn1WmxxRhq2Wqf3Q.QX2kDM1wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to delete a file/object in the directory using the rm command.

## References

None

## Moving Files - Challenge 9   
### This challenge requires us to move a specified file into a given location and then check to get the flag.

**Flag:** `pwn.college{4Qp7llKEOMVaOe-Vf4BeS-VPHeS.0VOxEzNxwyN4gjNzEzW}` 

The process of obtaining the flag involved moving a givewn file into a different one and then checking it to obtain a flag.

```
hacker@commands~moving-files:~$ ls
a  b
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{4Qp7llKEOMVaOe-Vf4BeS-VPHeS.0VOxEzNxwyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to move a file to a given location using the mv command.

## References

None

## Hidden Files - Challenge 10   
### This challenge requires us to find the hidden flag file to get the flag.

**Flag:** `pwn.college{AXNfJWp-ZRcRDrbBBcs08Nso4M6.QXwUDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved finding the contents of / using ls -a / and catting the flag file.

```
hacker@commands~hidden-files:~$ ls /
bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ ls -a /
.   .dockerenv             bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-154451067232036  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ cat .flag-154451067232036
pwn.college{AXNfJWp-ZRcRDrbBBcs08Nso4M6.QXwUDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how to find hidden files and reading them.

## References

None

## An Epic filesystem Quest - Challenge 11   
### This challenge requires us to find the hidden flag file to get the flag.

**Flag:** `pwn.college{wKFA-EXPdfSduktVQxKopwcS3ZU.QX5IDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved finding the contents of a hidden flag file using clues.

```
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
DISPATCH  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin       challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ ls -a
.   .dockerenv  bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
..  DISPATCH    boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@commands~an-epic-filesystem-quest:/$ cat DISPATCH
Lucky listing!
The next clue is in: /usr/lib/python3/dist-packages/pyasn1/codec/cer
hacker@commands~an-epic-filesystem-quest:/$ ls  /usr/lib/python3/dist-packages/pyasn1/codec/cer
BRIEF  __init__.py  __pycache__  decoder.py  encoder.py
hacker@commands~an-epic-filesystem-quest:/$ ls -a /usr/lib/python3/dist-packages/pyasn1/codec/cer
.  ..  BRIEF  __init__.py  __pycache__  decoder.py  encoder.py
hacker@commands~an-epic-filesystem-quest:/$ cat  /usr/lib/python3/dist-packages/pyasn1/codec/cer/BRIEF
Congratulations, you found the clue!
The next clue is in: /usr/share/rubygems-integration/all/gems/test-unit-3.3.5/lib/test/unit/util

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ ls -a /usr/share/rubygems-integration/all/gems/test-unit-3.3.5/lib/test/unit/util
.  ..  .SECRET  backtracefilter.rb  method-owner-finder.rb  observable.rb  output.rb  procwrapper.rb
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/rubygems-integration/all/gems/test-unit-3.3.5/lib/test/unit/util/.SECRET
Great sleuthing!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/STIX-Web/Latin/Bold
hacker@commands~an-epic-filesystem-quest:/$ ls -a /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/STIX-Web/Latin/Bold
.  ..  CLUE  Main.js
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/STIX-Web/Latin/Bold/CLUE
Tubular find!
The next clue is in: /usr/lib/ruby/2.7.0/rdoc/markup
hacker@commands~an-epic-filesystem-quest:/$ ls -a /usr/lib/ruby/2.7.0/rdoc/markup
.                     block_quote.rb         list_item.rb        to_bs.rb                to_table_of_contents.rb
..                    document.rb            paragraph.rb        to_html.rb              to_test.rb
TRACE                 formatter.rb           parser.rb           to_html_crossref.rb     to_tt_only.rb
attr_changer.rb       hard_break.rb          pre_process.rb      to_html_snippet.rb      verbatim.rb
attr_span.rb          heading.rb             raw.rb              to_joined_paragraph.rb
attribute_manager.rb  include.rb             regexp_handling.rb  to_label.rb
attributes.rb         indented_paragraph.rb  rule.rb             to_markdown.rb
blank_line.rb         list.rb                to_ansi.rb          to_rdoc.rb
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/lib/ruby/2.7.0/rdoc/markup/TRACE
Great sleuthing!
The next clue is in: /usr/lib/debug/.build-id/b5

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/lib/debug/.build-id/b5
hacker@commands~an-epic-filesystem-quest:/usr/lib/debug/.build-id/b5$ ls -a
.  ..  90fc8e2afe393bc8ee4052de3a6de82c601f23.debug  TIP
hacker@commands~an-epic-filesystem-quest:/usr/lib/debug/.build-id/b5$ cat TIP
Lucky listing!
The next clue is in: /usr/lib/python3/dist-packages/sage/coding/source_coding/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/debug/.build-id/b5$ cd /usr/lib/python3/dist-packages/sage/coding/source_coding/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sage/coding/source_coding/__pycache__$ ls -a
.  ..  LEAD  __init__.cpython-38.pyc  all.cpython-38.pyc  huffman.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sage/coding/source_coding/__pycache__$ cat LEAD
Congratulations, you found the clue!
The next clue is in: /usr/lib/ruby/2.7.0/bundler/templates

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sage/coding/source_coding/__pycache__$ cd  /usr/lib/ruby/2.7.0/bundler/templates
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/2.7.0/bundler/templates$ ls
BLUEPRINT  Executable  Executable.bundler  Executable.standalone  Gemfile  gems.rb  newgem
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/2.7.0/bundler/templates$ ls -a
.  ..  BLUEPRINT  Executable  Executable.bundler  Executable.standalone  Gemfile  gems.rb  newgem
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/2.7.0/bundler/templates$ cat BLUEPRINT
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/Documentation/features/debug/kgdb

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/2.7.0/bundler/templates$ ls -a /opt/linux/linux-5.4/Documentation/features/debug/kgdb
.  ..  NUGGET-TRAPPED  arch-support.txt
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/2.7.0/bundler/templates$ ls /opt/linux/linux-5.4/Documentation/features/debug/kgdb/NUGGET-TRAPPED
/opt/linux/linux-5.4/Documentation/features/debug/kgdb/NUGGET-TRAPPED
hacker@commands~an-epic-filesystem-quest:/usr/lib/ruby/2.7.0/bundler/templates$ cat /opt/linux/linux-5.4/Documentation/features/debug/kgdb/NUGGET-TRAPPED
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{wKFA-EXPdfSduktVQxKopwcS3ZU.QX5IDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me to use ls, ls -a, cd commands together and have a lot of patience :/ .

## References

None

## Making Directories - Challenge 11   
### This challenge requires us to make a directory and create a file in it to get the flag.

**Flag:** `pwn.college{o5NrDDN3t9JhXFgdSI9yv8r5mTD.QXxMDO0wyN4gjNzEzW}` 

The process of obtaining the flag involved making a directory inside /tmp and making a file in it.

```
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ /tmp
bash: /tmp: Is a directory
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ cd pwn
hacker@commands~making-directories:/tmp/pwn$ touch colleg
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{o5NrDDN3t9JhXFgdSI9yv8r5mTD.QXxMDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how making directories using the mkdir command works.

## References

None

## Finding Files - Challenge 12   
### This challenge requires us to find a flag file.

**Flag:** `pwn.college{E6zGLs0-TVdwYPJwyY8dLTZZGyV.QXyMDO0wyN4gjNzEzW}` 

The process of obtaining the flag using the command find /- name flag.

```
hacker@commands~finding-files:~$ find / -name flag
find: ‘/root’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/tmp/tmp.TpSOPGOVKK’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
^C
hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ cd /usr/local/lib/python3.8/dist-packages/pwnlib/flag
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ ls
__init__.py  __pycache__  flag.py
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ ls -a
.  ..  __init__.py  __pycache__  flag.py
hacker@commands~finding-files:/usr/local/lib/python3.8/
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ cd
hacker@commands~finding-files:~$ find / -name flag
find: ‘/root’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/tmp/tmp.TpSOPGOVKK’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/7/task/7/fd’: Permission denied
find: ‘/proc/7/task/7/fdinfo’: Permission denied
find: ‘/proc/7/task/7/ns’: Permission denied
find: ‘/proc/7/fd’: Permission denied
find: ‘/proc/7/map_files’: Permission denied
find: ‘/proc/7/fdinfo’: Permission denied
find: ‘/proc/7/ns’: Permission denied
/opt/linux/linux-5.4/drivers/scsi/mpt3sas/flag
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/nix/store/7ns27apnvn4qj4q5c82x0z1lzixrz47p-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/5z3sjp9r463i3siif58hq5wj5jmy5m98-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5n5lp1m8gilgrsriv1f2z0jdjk50ypcn-rizin-0.7.3/share/rizin/flag
/nix/store/h88mxp2mbgyj06vypwmqpy05idhwimnp-python3.13-pwntools-4.14.1/lib/python3.13/site-packages/pwnlib/flag
/nix/store/s8b49lb0pqwvw0c6kgjbxdwxcv2bp0x4-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/bnlabj2vsbljhp597ir29l51nrqhm89w-rizin-0.7.4/share/rizin/flag
/nix/store/1hyxipvwpdpcxw90l5pq1nvd6s6jdi5m-python3.12-pwntools-4.14.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5qz6hgb1qzpvjrsw20wyiylx5zw8b9bk-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
hacker@commands~finding-files:~$ /opt/linux/linux-5.4/drivers/scsi/mpt3sas/flag
bash: /opt/linux/linux-5.4/drivers/scsi/mpt3sas/flag: Permission denied
hacker@commands~finding-files:~$ cd /opt/linux/linux-5.4/drivers/scsi/mpt3sas/flag
bash: cd: /opt/linux/linux-5.4/drivers/scsi/mpt3sas/flag: Not a directory
hacker@commands~finding-files:~$ cat /opt/linux/linux-5.4/drivers/scsi/mpt3sas/flag
pwn.college{E6zGLs0-TVdwYPJwyY8dLTZZGyV.QXyMDO0wyN4gjNzEzW}
```

## What I Learned

The challenge taught me how to use the find command (find / -name filename). One of my mistakes was opening the python file named flag with cat which led to a huge mess.

## References

None

## Linking Files - Challenge 13   
### This challenge requires us symbolic link files and trick a file into giving us the flag.

**Flag:** `pwn.college{Ahi3LmbDtTaoXnyq4WQGE5uTfXB.QX5ETN1wyN4gjNzEzW}` 

The process of obtaining the flag using ls -l and linking the file to flag.

```
hacker@commands~linking-files:~$ ls -l /challenge/catflag
-rwsr-xr-x 1 root root 123 Jan 14  2025 /challenge/catflag
hacker@commands~linking-files:~$ ls -l /home/hacker/not-the-flag
ls: cannot access '/home/hacker/not-the-flag': No such file or directory
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ ls -l /home/hacker/not-the-flag
lrwxrwxrwx 1 hacker hacker 5 Sep 23 09:53 /home/hacker/not-the-flag -> /flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{Ahi3LmbDtTaoXnyq4WQGE5uTfXB.QX5ETN1wyN4gjNzEzW}
```

## What I Learned

The challenge taught me on how symbolic linking using ls -l works and can be used to read normally unsourceable data.

## References

None
# Decrypt an Encrypted Message

## Overview
Used Linux commands to locate a hidden file, decrypt a Caesar cipher, and recover an encrypted file with OpenSSL.

## Tools Used
- Linux Bash shell
- `ls`, `cat`, `tr`, `openssl`

## Commands Practiced
```bash
$ ls /home/analyst
# Output:
Q1.encrypted  README.txt  caesar

$ cat README.txt
# Output:
Hello,
All of your data has been encrypted. To recover your data, you will need to solve a cipher. To get started look for a hidden file in the caesar subdirectory.

$ cd caesar
$ ls -a
# Output:
.  ..  .leftShift3

$ cat .leftShift3
# Output:
Lq rughu wr uhfrvhu brxu ilohv brx zloo qhhg wr hqwhu wkh iroorzlqj frppdqg:

$ cat .leftShift3 | tr "d-za-cD-ZA-C" "a-zA-Z"
# Output:
In order to recover your files you will need to enter the following command:
openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute

$ cd ~
$ openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute
$ ls
# Output:
Q1.encrypted  Q1.recovered  README.txt  caesar

$ cat Q1.recovered
# Output:
Congratulations! You have successfully decrypted your files and recovered your data.
```

## Summary
Hands-on practice with finding hidden files, breaking a Caesar cipher using `tr`, and decrypting AES-256-CBC encrypted files with `openssl`. A very engaging and fun challenge.


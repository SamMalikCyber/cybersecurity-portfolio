# Create Hash Values

## Project Description
In this mini project, I used Linux commands to display file contents, generate SHA-256 hash values, save them to files, and compare them. This demonstrates file integrity verification.

## Tools Used
- `ls`
- `cat`
- `sha256sum`
- `cmp`

---

## Commands Practiced & Outputs
```bash
$ ls
# Output:
file1.txt  file2.txt

$ cat file1.txt
# Output:
X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*

$ cat file2.txt
# Output:
X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*

$ sha256sum file1.txt
# Output:
131f95c51cc819465fa1797f6ccacf9d494aaaff46fa3eac73ae63ffbdfd8267  file1.txt

$ sha256sum file2.txt
# Output:
2558ba9a4cad1e69804ce03aa2a029526179a91a5e38cb723320e83af9ca017b  file2.txt

$ sha256sum file1.txt >> file1hash
$ sha256sum file2.txt >> file2hash

$ cat file1hash
# Output:
131f95c51cc819465fa1797f6ccacf9d494aaaff46fa3eac73ae63ffbdfd8267  file1.txt

$ cat file2hash
# Output:
2558ba9a4cad1e69804ce03aa2a029526179a91a5e38cb723320e83af9ca017b  file2.txt

$ cmp file1hash file2hash
# Output:
file1hash file2hash differ: char 1, line 1
```

## Summary

In this mini project, I checked whether two files were identical by generating their SHA-256 hash values and comparing them. Even though both files looked the same when viewed with cat, their hashes were different, which confirmed that the files were not identical. I saved each hash to its own file, then used cmp to pinpoint the exact difference. This reinforced how hashing can reveal changes in files that aren’t obvious by inspection and showed how to verify file integrity with simple Linux commands.

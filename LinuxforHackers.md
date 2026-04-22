---
description: This is going to be a cheatsheet for important commands in linux with syntax.
---

# Linux for Hackers

whoami - prints the username of the currently logged-in user.

```bash
whoami
```

echo - outputs text or variable values to stdout.

```bash
echo "Hello World"
echo "text" >> file.txt
```

cd - changes the current working directory.

```bash
cd Desktop
cd .. 
cd ~
```

cat - concatenates and displays file contents.

```bash
cat file.txt
```

pwd - prints the absolute path of the current working directory.

```bash
pwd
```

grep - searches for patters in files using regex.

```bash
grep "root" /etc/passwd
```

diff - compares two files line by line.

```bash
diff file1.txt file2.txt
```

ls - lists directory contents.

```bash
ls 
ls -a 
```

touch - creates empty files or updates file timestamps.

```bash
touch payload.sh
touch -t 99999999 f
```

rm - removes files or directories.

```bash
rm file.txt
rm -rf /tmp/root
```

cp - copies files or directories.

```bash
cp file1.txt file2.txt
cp old.txt new.txt
```

mv - moves or renames files.

```bash
mv 1.txt 2.txt
```

mkdir - creates new directories.

```bash
mkdir test
```

find - searches for files by name, permissions, size, owner, or type.

```bash
find -name test
```

file - determines the true type of file regardless of extension.

```bash
file suspicious.bin
file image.jpg
```

ln - creates hard or symbolic links.

```bash
ln -s /etc/passwd /tmp/p
```

man - opens the namual page for any command.

```bash
man grep
man ls
```

help - displays help for bash built-in commands.

```bash
help cd 
```

#### Wildcard Characters

\* : matches any number of characters.

```bash
ls *.jpg
```

? : matches exactly one single character.

```bash
rm file?.txt
```

\[ ] : matches the character contained within the brackets.

```bash
cp [abc]* /tmp
```

\[! ] or \[^ ] : matches any character not listed inside the brackets.

```ballerina
ls [!0-9]*
```

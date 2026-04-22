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

### Wildcard Characters

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

### I/O Redirection and Stream Management

\| - Connects the standard output of one command directly into the standard input of another, creating a sequential chain of data.

```bash
cat names.txt | sort
```

\> - Overwrites a file with the standard output of a command.

```bash
ls > output.txt
```

\>> - Appends the standard output of a command to the end of an existing file.

```bash
echo "new line" >> log.txt
```

< - Redirects the contents of a file to be used as standard input for a command.

```bash
sort < list.txt
```

#### File Descriptor

A file descriptor is a non-negative integer that the Linux kernel uses as a unique identifier for an open file or I/O stream. By default, every process starts with three standard descriptors: `0` for Standard Input (stdin), `1` for Standard Output (stdout), and `2` for Standard Error (stderr). When you redirect output, you are essentially telling the shell to point these numeric indexes toward a specific file instead of the terminal.

Usage: `ls -l /root 2> error.log` _(This uses file descriptor `2` to redirect only error messages to a file while letting normal output show on the screen.)_

sed - A stream editor used to parse and transform text within a data stream.

```bash
sed 's/apple/orange/' fruits.txt
```

tee - Reads standard input and writes it to both standard output and one or more files.

```bash
ls | tee directory_list.txt
```

#### Process substitution

Process Substitution allows you to take the output of a command and feed it into another program as if it were an actual file. It creates a temporary "alias" for the data, which is useful for commands that expect a file path as an argument rather than a direct stream of text.

usage: cat <(echo hi)

mkfifo - Creates a named pipe (a special file) that allows independent processes to communicate.

```bash
mkfifo my_pipe
```

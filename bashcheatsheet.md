# Bash cheatsheet

### Echo
```bash
# echo displays a line of text
echo 1
```
Output:<br>
`1`

### Pipes
```bash
# The pipe "|" sends the output of one command to another, in this case, it sends the output of echo to rev
# rev reverses the input
echo abcd | rev
```
Output:<br>
`dcba`

### Chmod
Chmod is a command used to change permissions permissions to a file or folder. usage is the following
`chmod options permissions file`
```bash
#This makes the file executable
chmod +x file.sh
```
Permissions can be in alphanumerical characters or with octal numbers. Permissions are as follows:
```
u=user
g=group
o=others

r=read
w=write
x=execute
```
So, if someone wanted to add read and write permissions to the user and group, but only read permissions to others, the command would be:
```Bash
chmod u=rwx,g=rwx,o=r file
```
The equivalent to this in octal would be:
```Bash
chmod 774 file
```
Where the numbers mean:
```
4: read
2: write
1: execute
0: no permissions
```

## find

What it does: helps you find a file by several options.

Syntax:
`find [where] [option]`

Example:
```bash
find . -name "example.txt"
./documents/example.txt
```

Options:
- `-name` finds a file by the name (case sensitive).
- `-iname` finds a file by the name (not case sensitive).
- `-size` finds a file by its size. Suffixes: c (bytes), k (KB), M (MB), G (GB). We can also put a minus or a plus before the size to get all files that are smaller or bigger than the size we specified. For example, `find -size -1024c` will show all files smaller than 1024 bytes (not including 1024 bytes). The same goes for plus: `find -size +1024c` will show all files bigger than 1024 bytes (not including 1024 bytes). If we are looking for empty files/directories, we can simply type command `find -empty`.
- `-type` finds a file by the type: f (file), d (directory).
- `-perm` finds a file by permission: 4 (reading), 2 (writing), 1 (execute).
- `-user` finds a file by ownership.
- `-group` finds a file by group.
- `-[option]time` find a file by the time: `-mtime -7` - modified in the last 7 days, `-atime +30` - accessed more than 30 days ago, `-ctime 1` - status changed 24-48 hours ago.

P.S. We can also use logical operations in find commands:
- `find . ! -executable` finds files that are not executable (`!` stands for NOT logical operator).
- `find . -name "example.txt" -o -name "example.md"` finds file that are example.txt or example.md (`-o` stands for OR logical operator).

## grep

What it dose: finds a particular line in the file

Syntax:
`grep [option] [text] [file]` 

Example:
```bash
cat example.txt
admin 
user
admin123
guest
grep admin example.txt
admin 
admin123
```

Options:
- `-n` shows number of the line
- `-i` does not distinquish between uppercase and lowercase letters 
- `-r` tries to capture particular text from the whole folder 
- `-v` shows the rows that doesn't contains the specified text 
- `-c` displays the amount of lines that have the specified text
- `-w` finds the precise word `grep -w admin example.txt` wont give admin123 
- `-l` names of the files where there is a match 
- `-o` displays the specified word. The difference between -o and -w lets take for example file example.txt that contans lines:	
	1.superadmin 
	2.admin 
	3.admin is here
```bash
grep -w "admin" example.txt 
admin 
admin is here 

grep -o "admin" example.txt 
admin 
admin 
admin 
```

P.S. We can use multiple options in one command for example: grep -lr "admin" ., `grep -io "admin" example.txt`

## sort 

What it does: sorts a file by lines

Syntaxsis:
`sort [option] [file]`

Example:
```bash
cat file.txt 
orange
banana 
apple 

sort file.txt 
apple 
banana 
orange
```

Options:
- `-n` compare as a numbers. When we are using sort command it sorts by the firts letter/number in a row for example:
```bash
cat example.txt 
9
10
2
3
100

sort example.txt
10
100
2
3
9
```
this to fix this problem we need to use -n option 	
- `-r` makes an output oposite 
- `-u` deletes repetitions in the output
- `-f` does not distinquish between uppercase and lowercase letters 
- `-k N` sorts a file by collumn. Example:
```bash 
cat scores.txt
Michael 20 
Rauf 90
Said 60 

sort -k 2 -n -r scores.txt
Rauf 90
Said 60
Michael 20 
```
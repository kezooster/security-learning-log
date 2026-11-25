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

What it dose: finds a particular text in the file

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
- `-n` shows number of the row 
- `-i` does not distinquish between uppercase and lowercase letters 
- `-r` tries to capture particular text from the whole folder 
- `-v` shows the rows that contains no text 
- `-
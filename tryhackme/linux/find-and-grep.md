## find 

What it dose: helps you find a file by several options 

Syntax:
`find [where] [option]` 

Example:
```bash
find . -name "example.txt"
./documents/example.txt
```

Options:
- `-name` finds a file by the name (case sensitive)
- `-size` finds a file by the size, suffixes: c(bytes), k(KB), M(MB), G(GB)
- `-type` finds a file by the type: f(file), d(directory)
- `-perm` finds a file by permision: 4(reading), 2(writing), 1(execute)
- `-user Ed` finds a file by ownership
- `-[option]time` find a file by the time: `-mtime -7` - modified in the last 7 days, `-atime +30` - accessed more than 30 days ago, `-ctime 1` - status changed in 24-48 hours ago  

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
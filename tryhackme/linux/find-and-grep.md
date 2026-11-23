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
## pwd

What it does: shows which folder you are in now

Example:
```bash
pwd
/home/username
```

## ls

What it does: shows what is inside a folder

Syntax:
`ls [options] [folder]`

Example:
```bash
ls

project textfile.txt 
documents downloads
``` 

Options:
- `-l` shows more information about the files: permissions, owner, size, date
- `-a` shows all the files including hidden files 

## cd

What it does: helps you to navigate through folders 

Syntax:
`cd [folder]`

Example:
```bash
pwd
/home/bandit3
cd inhere
pwd
/home/bandit3/inhere
```

Shortcuts:
- `cd ..` goes one folder back
- `cd ~` or `cd` goes to the home folder
- `cd /` goes to the root folder 
- `cd -` goes to previous folder where you were before

## cat 

What it does: reads a file

Syntax:
`cat [filename]`

Example:
```bash
cat HelloWorld.txt
Hello World!
```

## touch 

What it does: creates an empty file (if the file already exists, it only updates its date)

Syntax:
`touch [files]`

Example:
```bash
touch notes.txt
ls
notes.txt
```

## mkdir 

What it does: creates a folder

Syntax:
`mkdir [option] [folder]`

Example:
```bash
mkdir project 
ls
project 
```

Options:
- `-p` creates a folder inside a path that you have chosen `mkdir -p project/ctf/web`

## cp

What it does: makes a copy of a file or a folder

Syntax:
`cp [option] [file/folder] [destination]`

Example:
```bash
cp notes.txt backup.txt 
ls
backup.txt notes.txt
```

Options:
- `-r` copies a folder with everything inside: `cp -r projects projects-backup`

## mv

What it does: moves and renames file or direcotry 

Syntax:
`mv [option] [source] [destination]`

Example:
```bash
ls
notes.txt  projects

mv notes.txt projects/
ls projects
notes.txt

mv projects/notes.txt projects/linux-notes.txt
ls projects
linux-notes.txt
```

## rm

What it does: removes a file or directory 

Syntax:
`rm [option] [source]`

Example:
```bash
ls 
example.txt
rm example.txt 
ls
   
```

Options:
- `-i` requires confirmation before deleting smth 
```bash 
rm -i example.txt 
remove regular empty file 'example.txt'? y 
ls

```
- `-r` removes directories and all the files inside them 
```bash 
ls project 
example.txt 
rm -r project 
ls 

```
- `-f` removes a file without confirmation 
```bash 
ls 
example.txt 
rm -f example.txt 
ls 

```

## pwd

What it dose: Shows in which folder are you now 

Example:
```bash
pwd
/home/username
```

## ls

What it dose: shows what is inside folder

Syntax:
`ls [options] [folder]`

Example:
```bash
ls

project tetxfile.txt 
documents downloads
``` 

Options:
- `-l` shows more information about the files: permision, owner, size, date
- `-a` shows all the files including hidden files 

## cd

What it dose: helps you to navigate through folders 

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

Options:
- `cd..` goes one folder back
- `cd ~` or `cd` goes to the home folder
- `cd /` goes to the root folder 
- `cd -` goes to previous folder where you was in 

## cat 

What it dose: reads a file

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

What it dose: creates folder

Syntax:
`mkdir [option] [folder]`

Example:
```bash
mkdir project 
ls
project 
```

Options:
- `p` creates a folder inside a path that you have chosen `mkdir -p project/ctf/web`

## cp

What it dose: makes a copy of a file or a folder

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





















 













































 

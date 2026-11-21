## Level 0 -> 1

The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

1. Used the `ls` command to look for files
2. Found the `readme` file
3. Used `cat readme` to read the file and found the password

## Level 1 -> 2

The password for the next level is stored in a file called - located in the home directory

1. Used `ls` and found a file called `-`
2. We can't read the file with `cat -` because `-` has a special meaning for cat, so I used `cat ./-`, where the dot stands for the current folder and `/` is the separator

## Level 2 -> 3

The password for the next level is stored in a file called --spaces in this filename-- located in the home directory

1. Used `ls` and found a file called `--spaces in this filename--`
2. Then used `cat ./'--spaces in this filename--'` to get the password. You can also use `cat -- '--spaces in this filename--'`

Mistake: I tried `cat '--spaces in this filename--'` and it didn't work. When cat reads the filename, it sees `--` and expects an option, but there is no such option, so it gives an error.

Fix 1: `cat ./'--spaces in this filename--'` works because the argument starts with a dot

Fix 2: `cat -- '--spaces in this filename--'` works because `--` marks the end of options, so the command runs properly

## Level 3 -> 4

The password for the next level is stored in a hidden file in the inhere directory.

1. Used `ls -la` and found the `inhere` directory
2. Used `cd inhere` and `ls -la` again to look for the password and found the `...Hiding-From-You` file
3. Finally, I used `cat ...Hiding-From-You` to get the password

## Level 4 -> 5

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the "reset" command.

1. Used `ls -la` and found the `inhere` directory, which contains 10 different files
2. Used `file ./-*` to find the only human-readable file (ASCII text)
3. Read the file `cat ./-file07` to get the password

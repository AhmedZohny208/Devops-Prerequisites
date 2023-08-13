## Shell Types
* Bourne Shell (Sh Shell)  --> Older (has limitation)
* C Shell (csh or tcsh)
* Z Shell (zsh)
* Bourne again shell (bash) --> Newer (Advanced)

You can see the shell type by:
```bash
echo $SHELL
```

## Commands
#### 1) Print to screen
```bash
echo Hi
```

#### 2) List files and folders
```bash
ls
```

#### 3) Change directory
```bash
cd my_dir2
```

#### 4) Present working directory (Print current directory)
```bash
pwd
```

#### 5) Make directory
```bash
mkdir new_directory
```

#### 6) Multiple Commands
```bash
cd new_directory; mkdir www; pwd
```

#### 7) Make directory hierarchy
Example: /tmp/asia/india/bangalore
```bash
mkdir /tmp/asia
mkdir /tmp/asia/india
mkdir /tmp/asia/india/bangalore
```

But instead we can type this
```bash
mkdir -p /tmp/asia/india/bangalore
```

#### 8) Remove directory
```bash
rm -r /tmp/my_dir1
```

#### 9) Copy directory
```bash
cp -r my_dir1 /tmp/my_dir1
```

## Commands Files
#### 1) Create a new file (no content)
```bash
touch new_file.txt
```

#### 2) Add content to file
```bash
cat > new_file.txt
```
Type content...
return: new line of text
CTRL + D: exit

#### 3) View content of file
```bash
cat new_file.txt
```

** For editing content of a file, you may need a text editor like VI or VIM

#### 4) Copy file
```bash
cp new_file.txt copy_file.txt
```

#### 5) Move (Rename) file
```bash
mv new_file.txt sample_file.txt
```

#### 6) Remove (delete) file
```bash
rm new_file.txt
```
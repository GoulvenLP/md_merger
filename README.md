# README

md_merger is a script that merges all **.md**-extension files that are contained in a specified directory and gathers them in a single destination file.

## 1. Installation
### 1.1. Download the project from git

```
git clone https://github.com/GoulvenLP/md_merger.git
```
### 1.2. Set the script privileges to executable

```
chmod 777 md_merger
```

### 1.3. Create an alias to manipulate the script easily
- Open a console
- Open the `.bashrc` file at the root of your session
- create an alias

```bash
alias md_merger="PATH_TO_THE_md_merger_FILE]"
```
- Close the terminal

Your script is ready to run!

## 2. Use
call the script with the name you used to define the alias
```bash
md_merger [PATH TO DIRECTORY] [DESTINATION FILE NAME]
```
- The path to the directory where the .md files are stored must be filled. <br/>
If you are already in the targetted directory, use `../directoryName` (replacing *directoryName* by your directory's name).
- Name the destination file you want to have. This parameter is optional. If this field is not filled, the destination file will be *"merged.md"*.

**nb**: files are merged alphabetically. To control the merge order take this 
information into account.

**e.g:**

```
00_file1.md
01_anotherFile.md
02_file.md
...
```
file `2-file.md` would be treated after file `02-file.md` for example.

The **md_merger** will merge all the .md files that are stored in the targeted directory and will gather them into a destination file. After the merge is done, the number of merged files will be displayed in the console.

**md_merger** can process with other format files present in the same directory: it targets the **.md** files.

## 3. Errors
Some error cases have been treated so that you can extract a maximum of informations to fix your troubles:
- Incorrect parameter value: **md_merger** expects between one and two parameters.
- The given targeted path is not a directory
- No .md files in the directory
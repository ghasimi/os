# os
Summary notes on operating systems

## Linux

### Files and Directories

```man COMMAND``` manual page of commands. e.g. ```man ls```.

```ls``` display non-hidden content of the directory.

```ls -a``` display all, inclduing hidden content.

```ls -l``` long format diplay.

```ls -lh``` long format diplay, with human-readable file sizes.

```ls -lt``` long format display, sorted by last modfied time.

```ls -alth``` display all, in long-format, sorted by time, with human-readable file sizes.

```ls -lS``` long format display, sorted by size.

```ls -l > filename``` output to a file.

```ls -l | sort -r -n +4``` list and sort by 4th column (size) in descending order (-r), based on numeric values (-n).  

```mkdir``` create directory.

```rmdir``` remove _empty_ directory.

```rm -d``` remove _empty_ directory.

```rm -r``` remove a directory and its content. ```-r``` stands for recursive.

```rm``` remove file.

```cd``` change directory.

```cd ..``` previous directory.

```cd /``` to the root directory.

```mv [source] [destination]``` move or rename.

```cp [source] [destination]``` copy.

```pwd``` print working directory.

```~/relative/path/from/home/username```.

```/relative/path/from/root```.

```find ~ -type f -name "ex*.csv" -size +100k``` find _csv_ files, in the home directory, with size greater than 100KB. 

```find . -maxdepth 3 -name "*apple*" -and -not -name "test*"``` find any file or directory, in the current path with max depth of up to two subfolders, that includes _apple_ and does not start with _test_.

```find . -iname "downl*"``` case-insensetive search to find any file or directory that starts with _downl_.

### Packages

```dpkg -l | less``` List of installed packages.

```sudo apt-get update``` Update packages list. 

```sudo apt-get install PACKAGE-NAME``` Install a package.


### ```Less``` command

``` | less ``` displays results one page at a time, e.g. ```dpkg -l | less```. Some navigation keys from [linode.com](https://www.linode.com/docs/guides/how-to-use-less/):

```space bar``` next page

```b``` previous page

```g``` first line

```G``` last line

```35p or 35%``` to 35% of the content.

```\search term``` search forward

```?search term``` search backward

```q``` Quit

### Multiple Commands

```A && B``` execute command B only if command A succeeded.

```A || B``` execute command B only if command A failed.

```A; B``` execute command B regardless of the status of command A.

```if [ -d path/to/folder ]; then  echo "folder exists"; else echo "folder does not exist"; fi```.


### Text


```nano``` terminal's editor.

```gedit``` GUI editor.

```cat``` print the content of files.

```echo "some texts" >> file``` append text to the end of the file.

```touch file1.txt file2.py file3``` create files.

Change the tab-size of `nano` by adding these lines to `~/nanorc`:

```
set tabsize 4
set tabstospaces
```

### Permissions Modes

- Permissions are based on three triads of read (r), write (w), and execute (x) for three the owner, group, and other. 
- For example ```-rwxrwxrwx``` gives all three r/w/x to all three owner/group/other.
- Each symbolic permission maps to a numeric code by summing up the bit values corresponding to the each permission. For example:

```
symbolic -rwxr--r-- maps to 744 as follows:

owner r: 100 -> 4
owner w: 010 -> 2
owner x: 001 -> 1
-> owner = 4 + 2 + 1 = 7

group r: 100 -> 4
group w: 000 -> 0
group x: 000 -> 0
-> group = 4 + 0 + 0 = 4

other r: 000 -> 4
other w: 000 -> 0
other x: 000 -> 0
-> other = 4 + 0 + 0 = 4

-> numeric = 744
```
 
- ```ls -l``` symbolic permission mode in the 1st column. 
- ```stat -c '%a %n' *``` numeric value of permission mode for all files in the folder.
- ```chmod 700 filename``` changes permission mode to 700.


### CPU Temperature

```
sudo apt-get install lm-sensors
sudo sensros-detect
sensors
```
To refresh every 1 seconds:
```
watch -n1 sensors
```


### Other

```ps``` list processes with PID, user, etc.

```top``` interactive summary of tasks and CPU/RAM utilization.

```gcc filename.c``` compile C.

```c++ filename.cpp``` compile C++.

```javac filename.java``` compile Java.

```gsettings set org.gnome.desktop.background picture-uri ""``` remove background picture.

```gsettings set org.gnome.desktop.background primary-color '#FF00BB'``` solid color for background.

```watch -n3 [command]``` to update the output of the command every 3 seconds.

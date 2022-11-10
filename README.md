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

### Other

```ps``` list processes with PID, user, etc.

```top``` interactive summary of tasks and CPU/RAM utilization.

```gcc filename.c``` compile C.

```c++ filename.cpp``` compile C++.

```javac filename.java``` compile Java.

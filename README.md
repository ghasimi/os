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


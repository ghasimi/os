# os
Summary notes on operating systems

## Linux

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


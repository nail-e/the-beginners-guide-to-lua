# Chapter 1 - Installing Lua
This chapter contains installation tutorials on how to install Lua on Windows, Linux and MacOS

## Installing on Windows
1. Go to the link http://luabinaries.sourceforge.net/#installation and install the latest release under the **History** section
2. Open the downloaded zip file
3. Create a folder called "Lua" in your C:\ directory (Friendly reminder that it is good practice to link your programming language binaries on Windows in C:\)
4. Extract the contents of the zip file in the newly created folder
5. Open System Properties and open Environment Variables
6. Edit the System Variables 'Path' variable
7. Add a new environment variable and link the Lua directory from C:\
8. In the terminal, run
```
C:\users\#USER#> lua
```

## Installing on Linux
1. Installing Lua using packages
In the terminal, run
```
$ sudo apt install lua5.3                             #Debian/Ubuntu systems 
```
```
# yum install epel-release && yum install lua         #RHEL/CentOS systems 
```
```
# dnf install lua                                     #Fedora 22+
```
1a. Installing Lua using sources
In the terminal, run
```
$ sudo apt install build-essential libreadline-dev    #Debian/Ubuntu systems 
```
```
# yum groupinstall "Development Tools" readline       #RHEL/CentOS systems 
```
```
# dnf groupinstall "Development Tools" readline       #Fedora 22+
```
1b. Builidng the sources
In the terminal, run
```
$ mkdir lua_build
$ cd lua_build
$ curl -R -O http://www.lua.org/ftp/lua-5.3.4.tar.gz
$ tar -zxf lua-5.3.4.tar.gz
$ cd lua-5.3.4
$ make linux test
$ sudo make install
```
2. In the terminal, run
```
$ lua
```

## Installing on MacOS (using terminal)
1. In the terminal, run
```
$ curl -R -O http://www.lua.org/ftp/lua-5.3.5.tar.gz
$ tar zxf lua-5.3.5.tar.gz
$ cd lua-5.3.5
$ make macosx install
```
2. In the terminal, run
```
$ lua
```

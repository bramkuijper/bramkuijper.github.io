# Lab projects using C++: a manual  

If you are doing a simulation/modeling project involving C++, you need to install/get acquainted with a bunch of programmes. This manual provides a brief description. 

Regardless of the operationg system you are using, make sure to read the [Now build a C++ program and run it](#RunC++) section below. ''Before'' doing so, however, first work through the [Installing things on Windows](#Windows) section. Otherwise continue right here with the [Installing things on a Mac](#Mac) section.

## <a name="Mac"></a>Installing things on a Mac
In short, we will do the following things:  
1. Use the Mac OS terminal application  
2. Install Xcode developer tools, which includes the c++ compiler ``clang``  
3. Install the package manager ``homebrew``  
4. Install ``git``  
5. Install some required libraries: ``yaml-cpp`` and ``libgsl``  
6. Install a coding editor like ``mate``  


### <a name="OSXTerminal"></a>Use the Mac OS terminal application
Open a Finder window. Then open the ''/Applications/Utitities'' folder. Then double-click ''Terminal''. A window like the one below should show up:  

![Figure of terminal window](https://raw.githubusercontent.com/bramkuijper/bramkuijper.github.io/master/devguide/img/terminal_screenshot.png) 

The text ``Macbook-Pro:~ bram$`` is called a prompt and informs you about the name of the computer you are working on (in this case ``MacBook-Pro``), the current directory (in this case ``~``: the home directory pointing to ``/Users/bram``) and the username (in this case ``bram``).

### Install Xcode developer tools
We need to install a c++ compiler with which we can translate c++ code into an executable file (i.e., an actual runnable program). To do so, you need to install command line tools for Xcode. For this, you need to register an apple developer account and download Xcode developer tools for command line. 

Installing Xcode is all very well described here:  
<https://www.mkyong.com/mac/how-to-install-gcc-compiler-on-mac-os-x/>

#### Was Xcode successfully installed?
We can see whether the c++ compiler was indeed successfully installed by launching a *new* ``Terminal`` window (see the [previous](#OSXTerminal) section on how to launch a terminal).

In the terminal, you should now type (and press enter afterwards):
```bash
g++
```
We should now see an error message like:
```bash
clang: error: no input files. 
```
In contrast to what you may believe, this is good news! The compiler is installed and just complains that you did not give it anything to compile.
However if you are getting the message:
```bash
-bash: g++: command not found
```
then the c++ compiler is *not* installed and you should check whether you have followed all steps in <https://www.mkyong.com/mac/how-to-install-gcc-compiler-on-mac-os-x/>.

### Install the package manager ``homebrew``
While most simulation models are rather basic, some rely on added functionality packaged in a number of  *libraries* that make life a bit easier. To compile and run the simulation models on your own computer you will need to install those libraries as well. This is done most easily by installing the ``homebrew`` package manager which manages the library installation for you.

1. Go to <https://brew.sh/>
2. Paste the little script that is presented there into the terminal and press enter.
3. You'r done. 

### Install ``git``
Git is a version control system -- it makes sure the source code you are running on your computer
Now that ``homebrew`` is installed, type
```bash
brew install git
```
in the terminal window. 

## <a name="Windows"></a>Installing things on Windows
1. Install MSYS2
2. Install the c++ compiler 'g++'
3. Install git
4. Install some required libraries: 'yaml-cpp' and 'libgsl'

### Install MSYS2



## <a name="Windows"></a>OK, installation done. Now build a c++ program and run it.
1. First, acquainted with some commonly used Unix commands




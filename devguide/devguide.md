# Lab projects using C++: a manual  

If you are doing a simulation/modeling project involving C++, you need to install/get acquainted with a bunch of programmes. This manual provides a brief description. 

Regardless of the operationg system you are using, make sure to read the [Now build a C++ program and run it](#RunC++) section below. ''Before'' doing so, however, first work through the [Installing things on Windows](#Windows) section. If you have a Mac, however, continue right here with the [Installing things on a Mac](#Mac) section. If you run Linux, you are likely to know all this already.

## <a name="Mac"></a>Installing programs and libraries on a Mac
For Windows see [the section below](#Windows).

In short, we will do the following things:  
1. Use the Mac OS terminal application  
2. Install Xcode developer tools, which includes the c++ compiler ``clang``  
3. Install the package manager ``homebrew``  
4. Install some required libraries: ``yaml-cpp`` and ``gsl``  
5. Install a text editor like ``mate``  


### <a name="OSXTerminal"></a>Use the Mac OS terminal application
Open a Finder window. Then open the ''/Applications/Utitities'' folder. Then double-click ''Terminal''. A window like the one below should show up:  

![Figure of terminal window](https://raw.githubusercontent.com/bramkuijper/bramkuijper.github.io/master/devguide/img/terminal_screenshot.png) 

The text ``Macbook-Pro:~ bram$`` is called a prompt and informs you about the name of the computer you are working on (in this case ``MacBook-Pro``), the current directory (in this case ``~``: the home directory pointing to ``/Users/bram``) and the username (in this case ``bram``).

Most of the day-to-day things are going to take place in a terminal. Hence, after this project you can add 'experience working with UNIX systems' to your CV. 

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
While most simulation models are rather basic, some rely on added functionality packaged in a number of  *libraries*.  To compile and run the simulation models on your own computer you will need to install those libraries as well. This is done most easily by installing the ``homebrew`` package manager which manages the library installation for you.

1. Go to <https://brew.sh/>
2. Paste the little script that is presented there into the terminal and press enter.
3. Answer a bunch of questions 
4. You are done. 

### Use ``homebrew`` to install required libraries

We are now going to use ``homebrew`` to install two essential libraries, [yaml-cpp](https://github.com/jbeder/yaml-cpp) and [gsl](https://www.gnu.org/software/gsl/doc/html/index.html). The former allows us to read so-called YAML files, which is handy when feeding a file with parameters to our simulation. The second is the GNU scientific library, which is handy for calculating eigenvalues and other mathsy constructs.

To install both libraries, type in your terminal:
```
brew install yaml-cpp gsl
```
and you're done.

### Install a text-editor like Textmate


### Done
All programs and libraries should now have been installed on your mac. You can move on to the [section where we are building a c++ program](#RunCplusplus) below.


## <a name="Windows"></a>Installing programs and libraries on Windows
Requirements: Windows 10, 64bit PC and approximate 1Gb of free disk space.

1. Install MSYS2
2. Install the c++ compiler ``g++``
3. Install ``git``
4. Install some required libraries: ``yaml-cpp`` and ``libgsl``

### Install MSYS2
MSYS2 is an emulator that allows us to run UNIX commands on a windows machine. Using MSYS2 makes it easy to port c++ code and associated libraries across different systems.

1. Go to <http://msys2.org> and download the one-click installer ``msys2-x86_64-20xxxxx.exe``
2. Once the file is downloaded click on it to instlal
3. A rather paranoid warning message 'windows protected your PC' shows up (see image below. The warning occurs as Microsoft wants developers to pay them fees for such warnings not to appear. The developers of MSYS2 (rightly) thought otherwise. To get rid of the warning message, click on the **more info** link in the 



## <a name="RunCplusplus"></a>OK, installation done. Now build a c++ program and run it.
1. First, acquainted with some commonly used Unix commands




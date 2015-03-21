# Downloads #

## Navigation ##
  * [Return to Table of Contents](TableOfContents.md)
  * [Jump to Downloads](Downloads.md)

## Introduction ##

Kojak is provided open source for free. Advanced users may wish to compile the source code for their custom system, or modify it for their own purposes. Below are instructions for installation on a Linux-based system using the command-line. It is assumed that SVN software is already installed on the system. Kojak can also be compiled for other operating systems/development environments including, but not limited to, Microsoft Visual Studio for Windows. Specific development environment instructions are outside the scope of this document, as it is assumed users of those environments are already familiar with them.

**The Kojak manuscript is currently in review. To protect this process, a key component of the source code has been omitted. It will be placed in the repository upon acceptance for publication.**


## Details ##

### Step 1: Check out the Kojak repository ###
Check out the repository on the [Source](https://code.google.com/p/kojak-ms/source/checkout) page. Follow the provided instructions.

### Step 2: Check out the supporting software libraries ###
a. [MSToolkit](https://code.google.com/p/mstoolkit/source/checkout) - used to support multiple file formats.

b. [Hardklor](https://code.google.com/p/hardklor/source/checkout) - used for spectral processing functions.

Both of these software tools have their own source repositories, applications, and instructions for use. For compiling Kojak from source, they simply need to be compiled on the system you are using.


### Step 3: Build support software ###
Both MSToolkit and Hardklor come with Makefiles. Compile MSToolkit first. Go into the MSToolkit directory and execute the Makefile. For example:

```
MSToolkit> make
```

When MSToolkit has finished building, compile Hardklor. To do so, change to the Hardklor directory. Open the Makefile first and set the path to your MSToolkit directory.

```
LIBPATH = /yourpath/MSToolkit
```

Save the Makefile. Then make Hardklor by typing 'make' on the command line.

### Step 4: Update paths in the Kojak Makefile ###
Navigate to your Kojak directory. Open Makefile with any text editor. Edit 'MSTOOLKITPATH' and 'HARDKLORPATH' to the location of your MSToolkit and Hardklor directories:

```
MSTOOLKITPATH = /yourpath/MSToolkit
HARDKLORPATH = /yourpath/Hardklor
```

Save the changes in the Makefile.

### Step 5: Make Kojak ###
Type 'make' from the command line.
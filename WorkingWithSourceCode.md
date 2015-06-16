# Checking Out the Source #

To check out the source code you will need a [Subversion](http://subversion.tigris.org/) client. After everything is set, issue the following command to check out the source:

```
svn checkout http://jdde.googlecode.com/svn/trunk/ jdde
```

This is the resulting folder structure:
```
jdde
  |-- /java
  |      |-- /src
  |      |-- /test
  |      +-- /build.xml
  |
  |-- /native
  |      +-- /src
  |
  |-- /build.xml
  |-- /LICENSE
  +-- /WHATSNEW
```

The _java_ folder contains source and test code written in java and an ant build file (it is used when working with eclipse, and is described below). The _native_ folder contains source code written in C/C++.

The 3 files located in the root directory are used for building purposes.

# Building from Source #

This wiki won't go through [JDK](http://java.sun.com/) and [Apache Ant](http://ant.apache.org/) installations.

First of all, you will need a C/C++ compiler in order to build the project. If you don't already have, download one from [MinGW](http://www.mingw.org/). During the installation process, make sure you select to install the **g++ compiler**. After the installation has finished, add the bin folder of the compiler to the system path variable.

Also, set a JAVA\_HOME environment variable pointing to your JDK installation directory. This step is necessary because when compiling the native library, it needs to find the JNI (Java Native Interace) include files located in the JDK installation directory.

The ant build file requires an external task called [cpptasks](http://ant-contrib.sourceforge.net/cpptasks/index.html) to compile the native library. Download it, and add the jar file to the lib folder of your ant installation directory.

Everything is now set and you can run the ant build file located in the root directory. It will create a build folder containing a jar file, a dll file, a LICENSE file, a WHATSNEW file, and a zip file containing all the previous files.

# Working with Eclipse #

_missing_
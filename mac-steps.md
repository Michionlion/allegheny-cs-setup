# Software Installation Guide for Windows
## Department of Computer Science, Allegheny College

To install Homebrew, do BREW STEPS
To install Git, do GIT STEPS
To install Java, do JAVA STEPS
To install Gradle, do GRADLE STEPS
To install Travis CI, do RUBY STEPS then TRAVIS-CI STEPS

Students in CS111 should install Java, Git, Gradle, and Travis CI in that order. Other classes should install the relevant modules that are in use in that class.

### BREW STEPS

Homebrew is a package manager for macOS. It helps you download programs, such as Gradle, or Ruby.

##### INSTALL

Run the following command in your terminal window:

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### JAVA STEPS
##### UNINSTALL

Check if you have Java by running `$ which java` in your terminal window.
If this returns a version, uninstall Java by running the following commands:

```
$ sudo rm -fr /Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin 
$ sudo rm -fr /Library/PreferencePanes/JavaControlPanel.prefPane 
$ sudo rm -fr ~/Library/Application\ Support/Java
```

##### DOWNLOAD

Download [Java SE JDK 9](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
Maria has a USB drive with the DMG file, so we don't have to all download from the network. 

##### INSTALL

Open the DMG file. This should bring up the JDK installer.
Press "continue" to install Java.


##### ENVIRONMENT VARIABLES

Though the DMG added Java to your path, it is still good to set up the variable "JAVA_HOME" for the Gradle installation.
Run the following commands:
```
$ touch .profile
$ nano .profile
```

This should bring up nano, a simple text editor, that you can use to add to this file. Add the following line to `.profile`.
```
export JAVA_HOME="$(/usr/libexec/java_home -v 9)"
```

### GIT STEPS

##### INSTALL
Execute the exe file that was downloaded previously.
Ensure that you select `Git Bash Here`, `Git LFS (Large File Support)`, and both options starting with `Associate`. Other options are optional.

In the next step, choose either `Use Git from Git Bash only` or `Use Git from Windows Command Prompt`. These do exactly as they say.

In the following steps, the defaults should be chosen unless you understand the implications.

To test that this step was completed successfully, right-click on your desktop and select `Git Bash Here`. Then, in the terminal that appears, type `git --version`. If `git version 2.14.2.windows.1` is printed, you have completed this step. If not, ask for help.

### GRADLE STEPS



### RUBY STEPS

### TRAVIS-CI STEPS

### PYTHON STEPS

### R STEPS
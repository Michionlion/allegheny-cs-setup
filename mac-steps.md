# Software Installation Guide for macOS
## Department of Computer Science, Allegheny College

Students in CS 111 with macOS should install Homebrew, Java, Git, Gradle, and Travis CI in that order. Other classes should install the relevant modules that are in use in that class.

## BREW STEPS

Homebrew is a package manager for macOS. It helps you download programs, such as Gradle, or Ruby.

#### INSTALL

Run the following command in your terminal window:

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## JAVA STEPS
#### UNINSTALL

Check if you have Java by running `$ which java` in your terminal window.
If this returns a version, uninstall Java by running the following commands:

```
$ sudo rm -fr /Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin 
$ sudo rm -fr /Library/PreferencePanes/JavaControlPanel.prefPane 
$ sudo rm -fr ~/Library/Application\ Support/Java
$ cd /Library/Java/JavaVirtualMachines/
$ sudo rm -rf <ALL FILES>
```

#### DOWNLOAD

Download [Java SE JDK 9](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
Maria has a USB drive with the DMG file, so we don't have to all download from the network. 

#### INSTALL

Open the DMG file. This should bring up the JDK installer.
Press "continue" to install Java.


#### ENVIRONMENT VARIABLES

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

## GIT STEPS

#### INSTALL

Run the follow command: 
```
$ brew install git
```

#### USAGE

##### SSH
You will need to set up a SSH key on your laptop. To do this, run the command:

```
$ ssh-keygen -t rsa
```

Press enter when prompted to enter the file in which to save the key. Press enter twice more when it says to enter a passphrase.

Then, run the command `$ cat /Users/<YOUR USERNAME/.ssh/id_rsa.pub`. This should display your public SSH key. Copy to your clipboard from the `ssh-rsa` to the last letter of the long string of random letters. Go to `github.com` and navigate to (upper right hand corner) `Settings > SSH and GPG keys` and press the `New SSH key` button. Give your new SSH key a cool title (e.g. "Maria's Macbook") and paste from your clipboard the SSH key you just copied. Then, press `Add SSH key`.

##### ACCESSING A REPOSITORY

To clone a repository, go to the repository's page and press `Clone or download`. In the "Clone with SSH" option, copy the repository URL to your clip board. Then, open a terminal and change into the directory you want to store your repository in. Type the following command `$ git clone <GITHUB REPOSITORY URL HERE>`. Now, you can change into the repository and do your usual `git add`, `git commit` and `git push` commands. 

## GRADLE STEPS

#### INSTALL

Run the follow command: 
```
$ brew install gradle
```

## TRAVIS-CI STEPS

#### INSTALL

Run the follow command: 
```
$ gem install travis -v 1.8.8 --no-rdoc --no-ri
```

Change into a repository where Travis CI is being used and run:

```
$ travis login --pro
``` 

Enter your GitHub credentials.

# Software Installation Guide for Windows

## Department of Computer Science, Allegheny College

Please follow the installation instructions for the tools listed under **Everyone** and your specific computer science course. Make sure to install the tools in the order they are listed.

**Everyone**
- [Git](#GIT-STEPS)
- A text editor of your choice (I recommend [Notepad++](#notepad-steps))

**CMPSC 111 and CMPSC 112**
- [Java](#java-steps)
- [Gradle](#gradle-steps)

### JAVA STEPS

#### DOWNLOAD

Download [Java SE JDK 9](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

Make sure to select the correct version for Windows. JDK 8 may also be used - make sure to change the relevant directories in the following steps.

#### INSTALL

Execute the exe file that was downloaded previously, and click through the options. You can choose all defaults, or customize it to your liking - be sure to remember any directory changes for the next step!

To test that this step was completed successfully, open a command prompt (search `cmd`), and execute `$ java --version`. If `java version "9"` is printed (perhaps along with some other stuff), you have completed this step. If not, ask for help.

#### ENVIRONMENT VARIABLES

Right-click on Start, then select "System", then in the upper left of the window that appears select System info (You can also hit the windows key and PAUSE). In the window that appears, select Advanced system settings. In the window that appears choose "Environment Variables" on the bottom right. You can also try searching for "environment". In the window that appears, click "New" below the
bottom scroll box. Enter JAVA_HOME as the variable name, and browse to where the Java JDK was installed (default: `C:\Program Files\Java\jdk-9`). Select OK. Now find the entry with Variable name "Path" in the lower scroll box. Select it, and
press "Edit". Click "New", and write `%JAVA_HOME%\bin`. Select OK until the windows close. Your changes do not take effect until all the Windows Settings windows are closed.

To test that this step was completed successfully, open a command prompt (search `cmd`), and execute `$ javac -version`. If `javac 9` is printed, you have completed this step. If not, ask for help.

### NOTEPAD++ STEPS

#### DOWNLOAD

Download [Notepad++](https://notepad-plus-plus.org/download/v7.5.4.html)

You'll likely want either the 32-bit or 64-bit installers. If you don't know which that is, download the [32-bit N++ 7.5.4 Installer](https://notepad-plus-plus.org/repository/7.x/7.5.4/npp.7.5.4.Installer.exe).

#### INSTALL

Execute the exe file that was downloaded previously, and click through the options. You can choose all defaults, or customize it to your liking.

### GIT STEPS

#### DOWNLOAD

Download [Git](https://git-scm.com/download/win)

#### INSTALL

Execute the exe file that was downloaded previously. Ensure that you select `Git Bash Here`, `Git LFS (Large File Support)`, and both options starting with `Associate`. Other options are optional.

Click next, then select Notepad++ as your editor (or a different option if you desire and have it installed). In the next step, choose `Use Git and optional Unix tools from the Windows Command Prompt`. If you use your terminal often, and know what you're doing, then you may want to choose `Use Git from the Windows Command Prompt` to avoid adding things you might already have.

In the following two steps, the defaults should be chosen unless you understand the implications. Then, you should select the `Use Windows' default console window` unless you're familiar with `MinTTY`. Then continue, selecting the defaults again, until setup completes.

To test that this step was completed successfully, right-click on your desktop and select `Git Bash Here`. Then, in the terminal that appears, type `$ git --version`. If `git version` followed by some version number is printed, you have completed this step. If not, ask for help.

#### SSH Key

You'll need to generate an SSH key so that you are able to access Bitbucket and/or Github. To generate the key, first run the following command in a "Git Bash Here" command prompt window.

```
$ ssh-keygen -t rsa -b 4096 -C "your_email_used_to_create_website_account@example.com"
```

Hit `ENTER` three times to take all the defaults. Now, run `cat ~/.ssh/id_rsa.pub`: this command will show your SSH key in the terminal; copy everything from the beginning `ssh-rsa` to the end, including your username and machine name (which looks like `username@machine`). Then, you can navigate to the SSH Key entry on the website you are using (directions below), and paste the key into the provided text box.

##### Bitbucket

Click on your profile icon in the lower left, and select "Bitbucket settings". On the left sidebar, select "SSH keys". Click on "Add key".

##### Github

Click on your profile icon in the upper right, then select "Settings". On the left sidebar, select "SSH and GPG keys". Click on "New SSH key".

### GRADLE STEPS

#### DOWNLOAD

Download [Gradle](https://gradle.org/releases/)

Select the most recent "binary-only" link. Currently that is under `v4.5.1` ([direct](https://services.gradle.org/distributions/gradle-4.5.1-bin.zip?_ga=2.52152425.1188320942.1518130805-15040205.1517342238)).

#### INSTALL

Right-click the zip that you previously downloaded, and select "Extract All". Browse to `C:\Program Files`, and extract. This should create a folder named `gradle-4.5.1` in your Program Files directory.

#### ENVIRONMENT VARIABLES

Right-click on Start, then select "System", then in the upper left of the window that appears select System info (You can also hit the windows key and PAUSE). In the window that appears, select Advanced system settings. In the window that appears choose "Environment Variables" on the bottom right. In the window that appears, click "New" below the bottom scroll box. Enter GRADLE_HOME as the variable name, and browse to where the `gradle-4.5.1` folder was created (with the above steps: `C:\Program Files\gradle-4.5.1`). Select OK. Now find the entry with Variable name "Path" in the lower scroll box. Select it, and press "Edit". Click "New", and write `%GRADLE_HOME%\bin`. Select OK until the windows close.

To test that this step was completed successfully, open a command prompt (search `cmd`), and execute `$ gradle --version`. If `Gradle 4.5.1` is printed (perhaps after a few warning messages), you have completed this step. If not, ask for help.

### ADVANCED SETUP

For any users who want to make the most out of their windows install, you can use the internet to figure out how to install or use the following tools.

* [Windows WSL](https://docs.microsoft.com/en-us/windows/wsl/install-win10), a bash terminal (command-line only) for windows
* [Cmder](http://cmder.net/), a terminal emulator to make `git bash` and `cmd` work better together; highly configurable
* [VSCode](https://code.visualstudio.com/), a text/code editor similar to `atom` (`atom` doesn't work well on windows, but you can [try](https://atom.io/) it)
* [Chocolatey](https://chocolatey.org/), a package manager for windows (like `aptitude` on Ubuntu)
* [Dual Boot Ubuntu](https://www.lifewire.com/ultimate-windows-8-1-ubuntu-dual-boot-guide-2200654), we recommend Ubuntu 17.10, but any other flavor of Linux works - research before you start, and feel free to ask any questions!

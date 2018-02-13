# Software Installation Guide for Windows
## Department of Computer Science, Allegheny College

To install Git, do GIT STEPS  
To install Java, do JAVA STEPS  
To install Gradle, do GRADLE STEPS  
To install Travis CI, do RUBY STEPS then TRAVIS-CI STEPS  

Students in CS111 should install Git, Java, and Gradle in that order. Other classes should install the relevant modules that are in use in that class.  


## JAVA STEPS
#### DOWNLOAD
Download [Java SE JDK 9](http://www.oracle.com/technetwork/java/javase/downloads/index.html)  
Make sure to select the correct version for Windows. JDK 8 may also be used - make sure to change the relevant directories in the following steps.

#### INSTALL
Execute the exe file that was downloaded previously, and click through the options. You can choose all defaults, or customize it to your liking - be sure to remember any directory changes for the next step!

To test that this step was completed successfully, open a command prompt (search `cmd`), and execute `$ java -version`. If `java version "9"` is printed (perhaps along with some other stuff), you have completed this step. If not, ask for help.


#### ENVIRONMENT VARIABLES
Right-click on Start, then select "System", then in the upper left of the window that appears select System info (You can also hit the windows key and PAUSE). In the window that appears, select Advanced system settings. In the window that appears choose "Environment Variables" on the bottom right. You can also try searching for "environment". In the window that appears, click "New" below the bottom scroll box. Enter JAVA_HOME as the variable name, and browse to where the Java JDK was installed (default: `C:\Program Files\Java\jdk-9`). Select OK. Now find the entry with Variable name "Path" in the lower scroll box. Select it, and press "Edit". Click "New", and write `%JAVA_HOME%\bin`. Select OK until the windows close.

To test that this step was completed successfully, open a command prompt (search `cmd`), and execute `$ javac -version`. If `javac 9` is printed, you have completed this step. If not, ask for help.

## GIT STEPS
#### DOWNLOAD
Download [Git](https://git-scm.com/download/win)

#### INSTALL
Execute the exe file that was downloaded previously.
Ensure that you select `Git Bash Here`, `Git LFS (Large File Support)`, and both options starting with `Associate`. Other options are optional.

In the next step, choose either `Use Git from Git Bash only` or `Use Git from Windows Command Prompt`. These do exactly as they say.

In the following steps, the defaults should be chosen unless you understand the implications.

To test that this step was completed successfully, right-click on your desktop and select `Git Bash Here`. Then, in the terminal that appears, type `$ git --version`. If `git version 2.14.2.windows.1` is printed, you have completed this step. If not, ask for help.

#### SSH Key
You'll need to generate an SSH key so that you are able to access Bitbucket and/or Github. To generate the key, simply run `$ ssh-keygen` in a "Git Bash Here" command prompt window. Hit `ENTER` to take all the defaults, until the prompt finishes. Now, run `cat ~/.ssh/id_rsa.pub | clip`: this command will copy your SSH key to your clipboard. Then, you can navigate to the SSH Key entry on the website you are using (directions below), and paste the key into the provided text box.

*Bitbucket*  
Click on your profile icon in the lower left, and select "Bitbucket settings". On the left sidebar, select "SSH keys". Click on "Add key".

*Github*  
Click on your profile icon in the upper right, then select "Settings". On the left sidebar, select "SSH and GPG keys". Click on "New SSH key".


## GRADLE STEPS
#### DOWNLOAD
Download [Gradle](https://gradle.org/releases/)  
Select the most recent "binary-only" link. Currently that is under `v4.5.1` ([direct](https://services.gradle.org/distributions/gradle-4.5.1-bin.zip?_ga=2.52152425.1188320942.1518130805-15040205.1517342238)).

#### INSTALL
Right-click the zip that you previously downloaded, and select "Extract All". Browse to `C:\Program Files`, and extract. This should create a folder named `gradle-4.2` in your Program Files directory.

#### ENVIRONMENT VARIABLES
Right-click on Start, then select "System", then in the upper left of the window that appears select System info (You can also hit the windows key and PAUSE). In the window that appears, select Advanced system settings. In the window that appears choose "Environment Variables" on the bottom right. In the window that appears, click "New" below the bottom scroll box. Enter GRADLE_HOME as the variable name, and browse to where the `gradle-4.2` folder was created (with the above steps: `C:\Program Files\gradle-4.2`). Select OK. Now find the entry with Variable name "Path" in the lower scroll box. Select it, and press "Edit". Click "New", and write `%GRADLE_HOME%\bin`. Select OK until the windows close.

To test that this step was completed successfully, open a command prompt (search `cmd`), and execute `$ gradle -version`. If `Gradle 4.2` is printed (perhaps after a few warning messages), you have completed this step. If not, ask for help.

## RUBY STEPS
#### DOWNLOAD
Download [RubyInstaller](https://rubyinstaller.org/downloads/)  
Select the most recent version. Currently that is `2.4.2-2` ([direct](https://github.com/oneclick/rubyinstaller2/releases/download/rubyinstaller-2.4.2-2/rubyinstaller-2.4.2-2-x64.exe)).

#### INSTALL
Execute the exe file you downloaded previously, and choose the default options. After the installation is complete, ensure you select `Run 'ridk install'...` to make sure everything is installed.

After the installation completes, a command prompt window will open, with options `1, 2, 3`. Do not enter any numbers, just hit `ENTER`. Take the defaults in the MSYS2 installation window that appears. Then once that finishes, let the command prompt finish all the installations. Another prompt will appear afterwards, asking if you want to install anything else. If everything completed successfully, simply hitting `ENTER` will close the prompt.

To test that this step was completed successfully, open a command prompt (search `cmd`), and execute `$ ruby -v`. If `ruby 2.4.2p198 (2017-09-14 revision 59899) [x64-mingw32]` is printed, you have completed this step. If not, ask for help.

## TRAVIS-CI STEPS

#### INSTALL
Execute `$ gem install travis -v 1.8.8 --no-rdoc --no-ri` in a command prompt or terminal window.

Any Travis CI setup specific to classes should be done after all installations are verified complete (refer to your first practical if you're looking for this, or ask Professor Kapfhammer).

To test that this step was completed successfully, open a command prompt (search `cmd`), and execute `$ travis version`. If `1.8.8` is printed, you have completed this step. If not, ask for help.
[

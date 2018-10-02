# Software Installation Guide for Windows

## Department of Computer Science, Allegheny College

Please follow the installation instructions for the tools listed under **Everyone** and your specific computer science course. Make sure to install the tools in the order they are listed.

### Everyone

- [Chocolatey](#chocolatey)
- [Git](#git)
- A text editor of your choice (I recommend [Notepad++](#notepad) or [Atom](https://atom.io/))
- [Java](#java)
- [Gradle](#gradle-steps)
- [GatorGrader dependencies](#gatorgrader)

### Chocolatey

#### Install

Open a command prompt window in administrator mode. To do this, search for "cmd" in the start menu, then right-click and select "Run as Administrator". Then, copy and paste the following command (without the starting `$`) into that terminal, and hit `enter`.

```
$ @"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```

#### Check

To test that this step was completed successfully, open a new command prompt (search `cmd`), and execute `choco --version`. If `0.10.11` is printed (or some other higher version), you have completed this step. If not, ask for help.

### Java

#### Install

Run the following command in a command prompt window in administrator mode.

```
$ choco install jdk8 -y
```

#### Check

To test that this step was completed successfully, open a new command prompt (search `cmd`), and execute `java --version`. If `java version "8"` is printed (perhaps along with some other stuff), you have completed this step. If not, ask for help.

### NOTEPAD++

#### Install

Run the following command in a command prompt window in administrator mode. **Only do this if you want to use Notepad++**.

```
$ choco install notepadplusplus -y
```

### Atom

#### Install

Run the following command in a command prompt window in administrator mode. **Only do this if you want to use Atom**.

```
$ choco install atom -y
```

### Git

#### Install

Run the following commands in a command prompt window in administrator mode.

For advanced users, you may wish to visit the [git package docs](https://chocolatey.org/packages/git) and check out what other params you can add, for your custom installation.

```
$ choco install git -y --params "/GitAndUnixToolsOnPath /WindowsTerminal /NoShellIntegration"
```

#### Check

To test that this step was completed successfully, open a new terminal and type `git --version`. If `git version` followed by some version number is printed (or something similar), you have completed this step. If not, ask for help.

#### SSH Key

You'll need to generate an SSH key so that you are able to access Bitbucket and/or Github. To generate the key, first run the following command in a command prompt window.

```
$ ssh-keygen -t rsa -b 4096 -C "your_email_used_to_create_website_account@example.com"
```

Hit `ENTER` three times to take all the defaults. Now, run `cat ~/.ssh/id_rsa.pub`: this command will show your SSH key in the terminal; copy everything from the beginning `ssh-rsa` to the end, including your username and machine name (which looks like `username@machine`). Then, you can navigate to the SSH Key entry on the website you are using (directions below), and paste the key into the provided text box.

##### Bitbucket

Click on your profile icon in the lower left, and select "Bitbucket settings". On the left sidebar, select "SSH keys". Click on "Add key".

##### Github

Click on your profile icon in the upper right, then select "Settings". On the left sidebar, select "SSH and GPG keys". Click on "New SSH key".

### Gradle

#### Install

Run the following commands in a command prompt window in administrator mode.

```
$ choco install gradle -y
```

#### Check

To test that this step was completed successfully, open a new terminal and type `gradle --version`. If `Gradle 4.10` is printed (perhaps after a few warning messages about Java), you have completed this step. If not, ask for help.

### GatorGrader

To run GatorGrader on Windows, you will need to install Python, Ruby, mdl, Pipenv, and proselint.

#### Install

Run the following commands in a command prompt window in administrator mode. A small note, however: if you run the last command (`mklink`) and get something like "No directory found", run `where python` to find what should replace `C:\Python36`; note that the printed directory will include `\python.exe` which you should not include. The goal is to create a link named `python3.exe` that points to `python.exe` in the installation directory. If you have any trouble with this step let a TA know!

```
$ choco install python -y --version 3.6.3
$ choco install ruby -y
$ mklink "C:\Python36\python3.exe" "C:\Python36\python.exe"
```

Now you should close and reopen another administrator teminal window and run the following commands:

```
$ pip install proselint
$ pip install pipenv
$ gem install mdl
```

#### Notes

GatorGradle is fairly untested on Windows, and so may exhibit bugs or otherwise not correctly work. If you encounter any issues, please raise an issue on the GatorGradle [issue tracker](https://github.com/GatorEducator/gatorgradle/issues)!

### End

You've now installed all the necessary tools for basic lab completion in CS100 and 101, and can probably fudge together another few if needed for more advanced classes. If you get an error when you are trying to use these tools, first try Googling the error. Chances are that you are not the first person to encounter the issue and someone has already asked how to solve it on StackOverflow or the GitHub issue tracker. If you are still stuck, feel free to send Saejin a message on Slack, or email us at my school email (`mahlauheinerts@allegheny.edu`) if we are not part of any of your Slack teams. Any CS Teaching Assistant should also be able to help.

For any users who want to make the most out of their windows install, you can use the internet to figure out how to install or use the following tools. These are purely optional (and sometimes not even recommended), but using [Chocolatey](https://chocolatey.org/packages) can make your lives much, much easier!

- [Cmder](http://cmder.net/), a terminal emulator to make `cmd` and `powershell` work better together; highly configurable
- [Dual Boot Ubuntu](https://www.lifewire.com/ultimate-windows-8-1-ubuntu-dual-boot-guide-2200654), we recommend Ubuntu 18.04, but any other flavor of Linux works - research before you start, and feel free to ask any questions!

### Uninstallation

If in the future you wish to uninstall anything you installed today, you can use the `choco uninstall <name>` command in an administrator terminal to uninstall the given package that you installed with chocolatey. This will render you unable to use those tools.

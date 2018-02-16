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

## GIT STEPS

#### INSTALL

Run the follow command: 
```
$ brew install git
```

#### USAGE

##### SSH
You will need to set up a SSH key on your laptop. The following comes from [Github's official guide on SSH keys](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/). Start by running the command:

```
$ ssh-keygen -t rsa -b 4096 -C "your_email_used_to_create_github_account@example.com"
```

Press enter when prompted to enter the file in which to save the key. Press enter twice more when it says to enter a passphrase.

Then, run the command `$ cat /Users/<YOUR USERNAME/.ssh/id_rsa.pub`. This should display your public SSH key. Copy to your clipboard from the `ssh-rsa` to the last letter of your email at the end. Go to `github.com` and navigate to (upper right hand corner) `Settings > SSH and GPG keys` and press the `New SSH key` button. Give your new SSH key a cool title (e.g. "Maria's Macbook") and paste from your clipboard the SSH key you just copied. Then, press `Add SSH key`.

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
$ sudo gem install travis -v 1.8.8 --no-rdoc --no-ri
```

Change into a repository where Travis CI is being used and run:

```
$ sudo travis login --pro
``` 

Enter your GitHub credentials.

## GATORGRADER Steps

To run GatorGrader correctly on Macs, you will need to install python3, gnu-getopt, mdl, and proselint.

#### INSTALL

Run the follow commands: 
```
$ brew install python3
$ brew postinstall python3
$ brew link python3
$ brew install gnu-getopt
$ brew link --force gnu-getopt
$ pip3 install proselint
$ gem install mdl
``` 
If you encounter permission problems, try appending `sudo` to the command.

## Fin

At this point, you should be able to clone git repositories. To actually write code, I recommend downloading [Atom](https://atom.io/) or [Sublime Text](https://www.sublimetext.com/)--these are text editors, just like GVim. For CMPSC 111 and 112, Atom should suffice. Sublime is a little bit faster than Atom in my experience, but you only notice this when you open up huge projects. And though Sublime is free, you have to pay $80 to avoid seeing a "Thanks for enjoying Sublime. Consider purchasing it." dialog every 20 saves (although you should really consider supporting the creators of Sublime because it's an awesome tool).

You can also use Vim in your terminal; to open a file, you type the command `$ vim <name of file>`. To start editing, you press the `i` key, and to save your work and close Vim, you press `ESCAPE` and then type `:wq` ("write" and "quit"). 

There you go! You are now all set to use your Mac to work on your class assignments. If you get an error when you're trying to use these tools, first try Googling the error. Chances are you're not the first person to encounter the issue and someone has already asked how to solve it on StackOverflow or GitHub issue tracker. If you're still stuck, feel free to send Saejin or me (Maria) a message on Slack, or email us at our school emails if we're not part of any of your Slack teams.

Good luck, and KCCO (Keep Calm and Computer On)!



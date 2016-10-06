# MacOS Setup Guides
### The setup guides about Node.js Web development for MacOS users.

---

> If you are Windows user, see [Windows Setup Guides](https://github.com/kouMatsumoto/windows10-setup-guide)  
> If you are Ubuntu user, see [Ubuntu Setup Guides](https://github.com/kouMatsumoto/ubuntu-setup-guide)

---


## Table of Contents

  1. [First MacOS System Settings](#first-macos-system-settings)
    1. [System Language](#system-language)
    1. [Create bash_profile](#confirm-bash_profile)
  1. [Install core software to Web development](#install-core-software-to-web-development)
    1. [Google Chrome](#google-chrome)
    1. [Homebrew](#homebrew)
    1. [Git](#git)
    1. [nvm](#nvm)




# First MacOSX System Settings
Before installing applications to development, Make sure your MacOSX is ready.


### System Language
In codeing, you should use English anywhere even on comments to avoid useless confusion.  
I recommend to set System language English as primary language.


### Create bash_profile
'~/.bash_profile' is used to set user environment variables. As default, '~/.bash_profile' doesn't exist.  
Check whether '~/.bash_profile' exists by ls command.
```
$ ls ~/.bash_profile
```
If file is not found, create new.
```
$ touch ~/.bash_profile
```
Then, make sure the file is created by above ls command.


**[Back to top](#table-of-contents)**




# Install core software to Web development
These are necessities in Node.js Web development.


### Google Chrome
Google Chrome is a popular browser but very strong tool as debugger.  
Google Chrome can debug HTML, CSS, JavaScript and even Node.js server.

Get from [here](https://www.google.com/chrome/browser/desktop/index.html)


### Homebrew
Homebrew is one of package managers for MacOS that make your software management easy.  
There are several steps in installing Homebrew.

First, install Xcode from App Store.  
Xcode is needed to install Command Line Tools, and Command Line Tools is needed so that your Mac could use gcc, make, other commands.

After installing Xcode, run below command to install Command Line Tools.
```
$ xcode-select --install
```

After installing Command Line Tools, run install command for Homebrew.
```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
The above command may be a little bit old.  
Confirm latest installation from [here](http://brew.sh/index.html).

Then, Verify you can use brew by next command.
```
$ brew -v
```


### Git
Git is modern version control system.

Install with Homebrew.
```
$ brew install git
```

Verify the installation was successful by next command.
```
$ git --version
git version 2.9.2
```


### nvm
nvm stands for Node.js Version Manager and it helps you to manage Node.js environment.  
I highly recommend to use nvm instead of raw Node.js.

See installation in [github.com](https://github.com/creationix/nvm).

After installing, then install Node.js through nvm.
Check Node.js versions you can install.
```
$ nvm ls-remote
```

Select a version to install, or use latest.
```
$ nvm install vX.X.X
$ nvm install node
```

Switch to installed Node.js version to use.
```
$ nvm use vX.X.X
```

Make sure you can use Node.js.
```
$ node -v
$ npm -v
```


**[Back to top](#table-of-contents)**

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
    1. [nvm](#nvm)




# First MacOSX System Settings
Before installing applications to development, you should confirm your MacOSX is ready.
Make sure all settings have been set.


### System Language
In programming, you should use English to write codes anywhere include inner comments.
To avoid useless confusion, it's better to set System language English as primary language.

### Create bash_profile
'~/.bash_profile' is used to set user environment variables.
As default, '~/.bash_profile' doesn't exist.
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
These are core applications in Node.js Web development.


### Google Chrome
Google Chrome is a popular browser but very strong tool as debugger.
This can debug HTML, CSS, JavaScript and even Node.js server.

Get from [here](https://www.google.com/chrome/browser/desktop/index.html)


### Homebrew
Homebrew is one of package managers for MacOS
To install and manage other software, this make your work easy.
To install Homebrew, there are several steps.

First, install Xcode from App Store.
Xcode is needed to install Command Line Tools, and Command Line Tools is needed so that your Mac could use gcc, make, and other commands.

After installing Xcode, run below command to install Command Line Tools.
```
$ xcode-select --install
```

After installing Command Line Tools, run install command for Homebrew.
```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
There is a possibility The command above is old.
Confirm latest install command from [here](http://brew.sh/index.html)

After installing Homebrew, Check whether you can use brew command.
```
$ brew -v
```



### nvm
nvm stands for Node.js Version Manager.
This helps you to manage Node.js development environment.

I highly recommend to use nvm instead of raw Node.js.

See installation in [github.com](https://github.com/creationix/nvm)

After installing nvm, then install Node.js through nvm.
Check Node.js versions you can install.
```
$ nvm ls-remote
```

Select a version to install, or use latest
```
$ nvm install vX.X.X
$ nvm install node
```

Switch to installed Node.js version to use
```
$ nvm use vX.X.X
```

Make sure you can use Node.js
```
$ node -v
$ npm -v
```



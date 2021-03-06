# apt-repo
This experimental repo contains the Open Source Components used to build a Monroe Node (Debian stretch)

## To add the repository to a system/node
As this is a experimental repo the packages are not signed. To configure apt to trust the repo by add the switch ```[trusted=yes]```

### add the repo:
* Debian : ```echo 'deb [trusted=yes] https://raw.githubusercontent.com/MONROE-PROJECT/apt-repo/master stretch main' > /etc/apt/sources.list.d/monroe.list```
    * or ```cd /etc/apt/sources.list.d/; wget https://raw.githubusercontent.com/MONROE-PROJECT/apt-repo/master/monroe.list```
* Ubuntu : ```echo 'deb [arch=amd64, trusted=yes] https://raw.githubusercontent.com/MONROE-PROJECT/apt-repo/master bionic main' > /etc/apt/sources.list.d/monroe.list```
    * or ```cd /etc/apt/sources.list.d/; wget https://raw.githubusercontent.com/MONROE-PROJECT/apt-repo/master/monroe-ubuntu.list```

## To add packages to the repo
Instructions taken from http://www.hackgnar.com/2016/01/creating-remote-apt-package.html

### 1. Install Dependancies for Creating our Repo
* Ubuntu/debian : sudo apt-get install reprepro
* Macos: brew install reprepro

### 2. Clone/update the repo
1. clone the repo or pull the lastest changes
2. cd apt-repo

### 3. Add your deb packages
* Debian: ```reprepro includedeb stretch <PATH_TO-DEB>/my_deb_package.deb```
* Ubuntu: ```reprepro includedeb bionic <PATH_TO-DEB>/my_deb_package.deb```

### 4. Commit and push

linux, ubuntu, apt, install, vscode

# Setup New Linux System

## VSCode Install

### A) BEST SOLUTION

- with `wget` and `dpkg`
- grab and instal latest VSCode:

```bash
wget 'https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64' -O /tmp/code_latest_amd64.deb
sudo dpkg -i /tmp/code_latest_amd64.deb
```

- can be saved to a file like `auto-update-vscode.sh` and run every time VSCode needs updating
- gets latest version unlike `apt` package manager

### B) with `apt` package manager

1. Update system repository

```bash
sudo apt update
```

Updates the system's repository and ensures, that the latest version of vscode is going to be installed.

2. Install pacakge dependencies
   For proper operation, vscode requires you to install package dependencies. Run the following command to resolve package dependencies:

```bash
sudo apt install software-properties-common apt-transport-https wget -y
```

3. Add repository
   Run the following command to add the Visual Studio Code repository to your system:

```bash
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
```

4. Install vscode

```bash
sudo apt install code
```

### Issues with Visual Studio Code on Linux

Run `code --verbose` to see error log when it won't start.

## Git Install

```bash
sudo apt install git
```

## Google Chrome Install


Use wget to download the latest Google Chrome `.deb` package :

```bash
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
```

Install Chrome .deb package on your system:

```bash
sudo apt install ./google-chrome-stable_current_amd64.deb
```


## How to Install Linux on Windows machine

Create bootable USB drive using `UNetbootIN`

## dpkg

- [basics](https://www.digitalocean.com/community/tutorials/dpkg-command-in-linux)

### list packages installed

```shell
# list all
dpkg -l
dpkg -l package-name
```

### remove package

```shell
# uninstall package
dpkg -r package-name

# uninstall program and remove configuration files
dpkg -P package-name
```

## Environmental Variables

[info](https://help.ubuntu.com/community/EnvironmentVariables)

```shell
# print all currently defined environmental variables
printenv

# print one specific environmental variable
printenv LANG
# or
echo $LANG


```

## How to install application

### Install JDK21 to Ubuntu

[Instruction](https://www.linuxcapable.com/how-to-install-openjdk-21-on-ubuntu-linux/)

Make sure `wget` is installed. If needed install with:

```shell
sudo apt install wget
```

#### Download and extract OpenJDK21 archive

Use [OpenJDK](https://jdk.java.net/) to get package to download.

```shell
# download
wget <package>.tar.gz
```

This will give you the name of the file saved.
like: `openjdk-21.0.1_linux-x64_bin.tar.gz`

```shell
# extract
tar <package>.tar.gz
```

#### Move the extracted files

```shell
# move to the directory files are extracted
# if it is under Downloads
cd Downloads/jdk-21.0.1

# create directory for files
sudo mkdir -p /usr/local/jdk-21

# move files
sudo mv * /usr/local/jdk-21
```

#### Set Environmental Variables

### [Alien](https://www.serverlab.ca/tutorials/linux/administration-linux/how-install-rpm-packages-on-ubuntu-using-alien/)

Ubuntu is a Debian based Linux distribution, and as such it uses `deb` packages for installing software.

Some software maintainers only provide an `RPM` package, a Debian package named `Alien` allows us to natively install RPM packages on Ubuntu.

It DID NOT WORK below:

```shell
# Install `Alien`
sudo apt-get install alien

# Convert `rpm` to `deb`
sudo alien <package>.rpm

# Install `deb` package
sudo dpkg -i <package>.deb

# OR convert and install in one step
sudo alien -i <package>.rpm
```

### How to install `tar` files

> `tar` are compressed files

1.  Download file
2.  `untar` it
    - go to `Downloads`
    - `tar -xvf <filename>`
3.  it will create a directory for the files, cd into it
    - it can give further instructions in a README
    - it can be ready to use

## Setup Terminal Profile to change font size

Terminal > Add profile > change font > set new profile default


2. Python was already installed

3. [npm](https://www.npmjs.com/)

```bash
sudo apt install npm
```

4. [docker](https://docs.docker.com/engine/install/ubuntu/)

5. yarn

```bash
npm install --global yarn
```

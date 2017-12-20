# Landkreuzer Wireless Machine

Small wirelles robot.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

To start work with project you need to install repo tool and yocto 

```
$ mkdir ~/bin
$ export PATH=~/bin:$PATH
$ curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
$ chmod a+x ~/bin/repo
$ sudo apt-get install gawk wget git-core diffstat unzip texinfo gcc-multilib \
     build-essential chrpath socat libsdl1.2-dev xterm
```

Also please follow this instructions to add ssh keys to GitHub: https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/

### Installing

Init repo manifest

```
$ repo init -u git@github.com:olegcherpak/manifest.git
```

sync work tree

```
$ repo sync -j8 -c
```

Setup build environment

```
$ cd poky
$ source setup-environment
$ bitbake landkreuzer-image
```

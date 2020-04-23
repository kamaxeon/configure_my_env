# Set up my environment
The main idea of this repository is to configure my work environment.

## Getting Started

You must download the repository and run the ansible playbook

```bash
git clone https://github.com/kamaxeon/config_my_laptop
cd config_my_laptop
ansible-playbook playbook.yml -b
```

### Prequisites 


Obviously, you need to have ansible and git installed on your machine, if you do not have it, you can do it quickly with:
```bash
sudo apt-get install -y git ansible
```

Your user must be in the sudoers group as admin

It is designed to work with Ubuntu, and has been tested with version 18.04

## Tags

The playbook has a list of labels, which allows us to launch only the part that interests us

For your use, you can specify them when launching the playbook:

```bash
ansible-playbook playbook.yml -b -t my_tag1,mytag2
```

You can also exclude:

```bash
ansible-playbook playbook.yml -b --skip-tags=my_tag1,mytag2
```

Below you can see all the labels

### base_packages

Install base pacakges

### chrome

Install chrome

### docker

Uninstall docker packages from distro and install packages from docker.com

### dropbox

Install dropbox

### Git

Install config files for git 

### password_management

I currently use [pasaffe](https://launchpad.net/pasaffe), and synchronize it via dropbox.

### python

Install:
  * Versión 2 y 3 .deb packages
  * Pyenv (if you do not use it, try it, it's amazing)
  * flake8
  * pip (2 and 3)
  * Virtualenv

### sudo

Configure to use sudo without a password, it is a workstation, not a server :-)

### tmux

I'm starting to use it, and I have a minimal configuration

### vagrant

Still, I used for some projects, that's the reason to keep it.

### vim

This is the most worked part, what it does is:
  * Use bundle to manage plugins
  * Adapt my development environment for python
  * Configuration for markdown files
  * NerdTree
  * Ansible support for playbook
  * Powerline
  * etc ... see [vimrc](dotfiles/vimrc)


### virtualbox

Uninstall docker packages from distro and install packages from virtualbox.com

### zsh

Install zsh and ohmyzsh, and configure my user to use it.

### code

Install vscode

## Authors 

* **Israel Santana** - [kamaxeon](https://github.com/kamaxeon)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

# Ubuntu fresh installation

## Drivers

To auto-detect and install recommanded drivers, run the following command:
```bash
sudo ubuntu-drivers autoinstall
```
Then you may reboot your computer.

## Useful packages

### Vim

First, you should install Vim:
```bash
sudo apt-get install vim
```

Then, you may copy the provided vimrc to your config files:
```bash
cp vim/vimrc ~/.vimrc
cp vim/vimrc_epita ~/.vimrc_epita
```

In order to correctly configure Vim, you may install Vundle. To install Vundle, type this command:
```bash
git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
You may do that before using vim or you'll get an error about missing packages.

### Git

You can install git with the following command:
```bash
sudo apt-get install git
```

Then, you may generate a new ssh key and add it to your github account
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
Then, add the generated key to the ssh-agent
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```

* git
* gcc
* i3
* feh
* compton
* nm-applet
* rofi


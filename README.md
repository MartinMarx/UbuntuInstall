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

### i3 configuration

You may first install a few packages in order to use the provided i3 config file
```bash
sudo apt-get install feh
sudo apt-get install compton
sudo apt-get install rofi
sudo apt-get install i3blocks
sudo apt-get install arc-theme
sudo add-apt-repository -u ppa:snwh/ppa
sudo apt-get install moka-icon-theme faba-icon-theme faba-mono-icons
sudo apt install arandr
sudo apt install thunar
```

Then you may install the FontAwesome font from the GitHub repo. Download the latest DESKTOP version [from the official repo](https://github.com/FortAwesome/Font-Awesome/releases).
Now, extract and install the new font:
```bash
unzip ~/Downloads/fontawesome-[version]
mkdir ~/.fonts
cp fontawesome-[version]/otfs/*.otf ~/.fonts/
```

You may also install a custom system font to make your i3 look better. For example, you can get the San Francisco font from [the official github repo](https://github.com/supermarin/YosemiteSanFranciscoFont). Then again, unzip the font and add it to your system.
```bash
unzip ~/Downloads/YosemiteSanFranciscoFont-master
cp YosemiteSanFranciscoFont-master/*.ttf ~/.fonts/
```

Now, to apply this font to your entire system, download and install lxappearance:
```bash
sudo apt-get install lxappearance
```

Then launch lxappearance at least once to generate the config file. Now edit the config file and update the default gtk2 font:
```bash
vim ~/.gtkrc-2.0
gtk-font-name="Sans 10" // replace this line
gtk-font-name="System San Francisco Display 12" // with this line
```

Then do the same with the gtk3 config file:
```bash
vim ~/.config/gtk-3.0/settings.ini
gtk-font-name="Sans 10" // replace this line
gtk-font-name="System San Francisco Display 12" // with this line
```

Now you can restart lxappearance and see that the default font has been updated

## Useful programs

### Atom

First, download atom package from [atom.io](https://atom.io/).
Then install it:
```bash
sudo dpkg -i ~/Downloads/atom-amd64.deb
sudo apt install atom
```


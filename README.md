# my-webdev-pro-mac-setup
How I setup my mac for web dev

## Table of contents
- [iTerm2](#iTerm2)
- [XCode](#XCode)
- [Mac Setup](#Mac-Setup)
- [Google Chrome](#Google Chrom-)
- [Brew](#Brew)
- [Pro Tools For Front-end Dev](#Pro-Tools-For-Front-end-Dev)
- [iTerm and Fish](#iTerm-and-Fish)
- [GIT](#GIT)
- [NodeJS & Yarn](#NodeJS-&-Yarn)
- [NVM](#NVM)
- [Android Studio](#android-studio)
- [Github](#github)
- [Mov To Gif](#mov-to-gif)
- [Chrono](#chrono)
  
## XCode
  - XCode from MacOs
  - The simulator can be open quickly with:
  ```
  open /Applications/Xcode.app/Contents/Developer/Applications/Simulator.app
  ```
  
## Mac Setup
- remove shortcup when press space bar:
settings > keyboard > text > Add dot when double-tap the space bar
- disable screensaver
```
sudo defaults write /Library/Preferences/com.apple.screensaver loginWindowIdleTime 0
```
- Allow apps downloaded from Anywhere (on secured Mac)
```
sudo spctl --master-disable
```
- Install Mini-calendar :
https://apps.apple.com/ca/app/mini-calendar/id1088779979?l=fr&mt=12

_ Script for Display Screeen
https://github.com/univ-of-utah-marriott-library-apple/display_manager
`display_manager.py res default ext0` : reset resolution on external display monitor

## Google Chrome
```
brew cask install google-chrome
```
- extensions : 
  - React Developer Tools
  - Redux DevTools
  - Fonts Ninja : https://chrome.google.com/webstore/detail/fonts-ninja/eljapbgkmlngdpckoiiibecpemleclhh/related

## Brew
  - brew: https://brew.sh/
  ```
  ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" < /dev/null 2> /dev/null
  ```
  - `brew update && brew upgrade` (update for already installed packages)

## Pro Tools For Front-end Dev
```
brew cask install yarn firefox google-chrome slack zeplin
```

## iTerm and Fish
https://github.com/nicolastrote/how-to-configurate-Oh-My-Fish

## GIT
Installation de GIT
```
brew cast install Git
```
Puis on le configure
```
$ git config --global color.ui true
$ git config --global user.name "YOUR NAME"
$ git config --global user.email "YOUR@EMAIL.com"
```
If you don't have ssh key, you should:
```
$ ssh-keygen -t rsa -C "YOUR@EMAIL.com"
```
The next step is to take the newly generated SSH key and add it to your Github account.
```
$ pbcopy < ~/.ssh/id_rsa.pub
```
Copy the key and paste it on your github or bitbucket or gitlab profil in settings. You be able to clone a repo with a ssh command like `git clone git@github.com:nicolastrote/my-mac-setup.git`

## NodeJS & Yarn 
  - NodeJS and Yarn: `brew install nodejs yarn`
  - postman:
    - `brew cask install postman`

## NVM
Nvm is usefull for switching between NodeJS versions
  - Install nvm via Homebrew
```
brew install nvm
```
  - Create system directory for nvm
```
mkdir ~/.nvm
```
  - Install Bass 
```
git clone https://github.com/edc/bass.git
cd bass
make install
```
  - Fish config
Add following line to your ~/.config/fish/config.fish
```
function nvm
  bass source (brew --prefix nvm)/nvm.sh --no-use ';' nvm $argv
end

	set -x NVM_DIR ~/.nvm
	nvm use default --silent
```
  - NVM version
`nvm --version`

## Android Studio
```
brew cask install android-studio
```

## Github
- open iTerm2 and `cd ~ && mkdir Workspace && cd ~/Workspace`
- `yarn init`
- `git clone https://github.com/nicolastrote/cat-fight.git && cd cat-fight`

## Tty-Clock
Smart Clock in terminal
brew install tty-clock

## Mov To Gif
- make and export "in.mov" file with quicktime
- `brew install ffmpeg`
- `brew install gifsicle`
- `ffmpeg -i input.mov -s 600x400 -pix_fmt rgb24 -r 10 -f gif - | gifsicle --optimize=1 --delay=3 > out.gif`

## Chrono
time sleep 60s | echo "I sleep 60s"

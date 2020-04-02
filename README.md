# my-mac-setup
How I setup my mac for web dev

## Table of contents
- [iTerm2](#iTerm2)
- [XCode](#XCode)
- [Brew](#Brew)
- [NodeJS & Yarn](#NodeJS-&-Yarn)
- [Github](#github)
- [Disable Screensaver](#disable-screensaver)
- [Mov To Gif](#mov-to-gif)
- [Chrono](#chrono)

## iTerm2
  - iTerm2: https://www.iterm2.com/downloads.html
  
## XCode
  - XCode from MacOs
  
## Brew
  - brew: https://brew.sh/
  ```
  ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" < /dev/null 2> /dev/null
  ```
  - `brew update && brew upgrade` (update for already installed packages)
  
 ## NodeJS & Yarn 
  - NodeJS and Yarn: `brew install nodejs yarn`
  - postman:
    - `brew cask install postman`

## Github
- open iTerm2 and `cd ~ && mkdir Workspacecd && cd ~/Workspace`
- `yarn init`
- `git clone https://github.com/nicolastrote/cat-fight.git && cd cat-fight`

## Tty-Clock
Smart Clock in terminal
brew install tty-clock

## Disable Screensaver
defaults -currentHost write com.apple.screensaver idleTime 0

## Mov To Gif
- make and export "in.mov" file with quicktime
- `brew install ffmpeg`
- `brew install gifsicle`
- `ffmpeg -i but\ back\ button-480.mov -s 600x400 -pix_fmt rgb24 -r 10 -f gif - | gifsicle --optimize=3 --delay=3 > out.gif`

## Chrono
time sleep 60s | echo "I sleep 60s"

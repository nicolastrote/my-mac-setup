# my-mac-setup
How I setup my mac for web dev

## Table of contents
- [iTerm2](#iTerm2)
- [XCode](#XCode)
- [Brew](#Brew)
- [NodeJS & Yarn](#NodeJS & Yarn)
- [Github](#github)

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

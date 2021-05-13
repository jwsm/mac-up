# New macOS Workstation Setup


## Applications

1Password
Chrome
Firefox
KeepingYouAwake
Alfred
iTerm 3
VSCode
Viscosity
Slack
Magnet
Evernote
Pocket
Docker Desktop
Medis
Fork


## Configuration

### Screenshots

```
mkdir ~/Screenshots
defaults write com.apple.screencapture location ~/Screenshots
defaults write com.apple.screencapture show-thumbnail -bool FALSE
killall SystemUIServer
```

Then drag the Screenshots folder into the dock, and view as a Fan, sorted by Date Added


### Keyboard Configuration

Shorten the key repeat rate and initial delay
```
defaults write -g InitialKeyRepeat -int 12
defaults write -g KeyRepeat -int 2
```

Enable press and hold to repeat keystrokes
```
defaults write NSGlobalDomain ApplePressAndHoldEnabled -bool false
```

> Logout/Login to apply


### Mouse Configuration

In System Preferences > Mission Control, set middle mouse button to open mission control.


### Do Not Disturb

Notification Settings


## Tools

### iTerm

- Download [iTerm 3](https://iterm2.com/version3.html)
- Import [profile](./config-files/iterm-profile.json)
- This requires the fonts below

### Homebrew

- Install Homebrew from https://brew.sh/
- Change ownership of `/usr/local/share/zsh` `/usr/local/share/zsh/site-functions` as brew suggests

### ZSH

- `zsh` is now bundled with macOS
- Install [Oh My ZSH](https://github.com/ohmyzsh/ohmyzsh)


### GitHub

- In GitHub Settings > Developer, create a new access token for the mac
- Configure `git` to use macOS Keychain to store access key ([see this](https://docs.github.com/en/free-pro-team@latest/github/using-git/caching-your-github-credentials-in-git))
    ```
    git config --global credential.helper osxkeychain
    ```
- Clone repos using https, using access key as password


### VSCode

- Install the command line tool (type shift-cmd-P `> install shell command`)

#### Configuration:
- Open projects in new window

#### Themes
- Atom One Dark
- Electron Color Theme
- Electron Highlighter Syntax
- Gruvbox Themes
- Hopscotch
- Noctis
- Simple Icons

#### Extensions
- Vetur
- GitLens
- Docker
- Terraform

### AWS CLI

Install AWS CLI
```
brew install awscli
```

### Other Command line tools

- Tig (`brew install tig`)


## Fonts

### Fixed Width Fonts
- [Droid Sans Mono for Powerline](https://github.com/powerline/fonts/blob/master/DroidSansMono/Droid%20Sans%20Mono%20for%20Powerline.otf)
- [Fira Code](https://github.com/tonsky/FiraCode)
- [IBM Plex Mono](https://github.com/IBM/plex/releases/latest)
- [Inconsolata](https://github.com/googlefonts/Inconsolata)
- [JetBrains Mono](https://www.jetbrains.com/lp/mono/)
- [Rec Mono Casual](https://www.recursive.design/)
- Rec Mono Linear
- Rec Mono SemiCasual
- [Roboto Mono](https://github.com/google/fonts/tree/master/apache/robotomono)
- SF Mono
- Ubuntu Mono


## References

- [macOS Setup Guide](https://sourabhbajaj.com/mac-setup/)


# Python

Use pyenv to manage python versions

Create a virtual environment:
```
mkdir ~/.virtualenvs
python3 -m venv ~/.virtualenvs/djangodev
source ~/.virtualenvs/djangodev/bin/activate
```

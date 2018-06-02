# cheat-sheet

> Useful things I don't want to remember.


## Crouton

### Install Xenial with LXDE and Xiwi

```
sudo sh ~/Downloads/crouton -t lxde,xiwi
```

### Start terminal in chroot

```
sudo startxiwi -n xenial -T xterm
```

### Start desktop environment

```
sudo startlxde
```

### More info

https://github.com/dnschneid/crouton/wiki/Crouton-Command-Cheat-Sheet


## zsh

### Install zsh

#### Ubuntu

```
sudo apt-get zsh

```

#### macOS

```
brew install zsh
```


### Install oh-my-zsh

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### Copy .zshrc

```
wget -P ~ https://raw.githubusercontent.com/drich14/cheatsheet/master/.zshrc
```


## Curl

### Install

```
sudo apt-get install curl
```

## wget

```
brew install wget
```

## Node Platform

### Install NVM

```
curl -sL https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh -o install_nvm.sh
bash install_nvm.sh
```

### Install Node (and NPM)

```
nvm install node
```

### Fix Ubuntu bug
```
ln -s /usr/bin/nodejs /usr/bin/node
```


## Yarn

### Install

#### Ubuntu

```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update && sudo apt-get install yarn
```

#### macOS

```
brew install yarn --without-node
```


## Git

### Install

#### Ubuntu

```
sudo apt-get install git
```

#### macOS

```
brew install git
```


## Commitizen

### Install Commitizen CLI (Globally) 

```
yarn global add commitizen
```

### Install (in project root)

```
commitizen init cz-conventional-changelog --save-dev --save-exact
```


## GPG Auto Git Signing

### Generate a new pgp key

```
gpg --gen-key
```

### Check current keys

```
gpg --list-secret-keys --keyid-format LONG
```

### Export public key in gpg
your_key_id is the HASH id in front of `sec` in previous command.

```
gpg2 --armor --export your_key_id | pbcopy
```

Paste on GitHub (https://github.com/settings/gpg/new)

### Set a pgp key for git

```
git config --global user.signingkey your_key_id
git config --global commit.gpgsign true
```

## SSH

### Generate key

```
ssh-keygen -t rsa -b 4096 -C "dylanrichardson1996@gmail.com"
ssh-add -K ~/.ssh/id_rsa
pbcopy < ~/.ssh/id_rsa.pub
```

Paste on GitHub (https://github.com/settings/ssh/new)

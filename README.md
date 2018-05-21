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

### More info

https://github.com/dnschneid/crouton/wiki/Crouton-Command-Cheat-Sheet


## zsh

### Install zsh

```
sudo apt-get zsh

```

### Install oh-my-zsh

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### Copy .zshrc

[.zshrc](.zshrc)


## Curl

### Install

```
sudo apt-get install curl
```

## Yarn

### Install

```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update && sudo apt-get install yarn
```

## Node Platform

### Install Node

```
sudo apt-get install nodejs
```

### Install NPM

```
sudo apt-get install npm
```

### Update NPM

```
npm install -g npm
```

### Install NVM

```
curl -sL https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh -o install_nvm.sh
bash install_nvm.sh
```

### Update Node

```
nvm install <version>
nvm use <version>
```

### Fix Ubuntu bug
```
ln -s /usr/bin/nodejs /usr/bin/node
```


## Git

### Install

```
sudo apt-get install git
```

### Install Commitizen CLI

```
yarn global add commitizen
```


## GPG Auto Git Signing

### Generate a new pgp key

```
gpg2 --gen-key
```

### Check current keys

```
gpg2 --list-secret-keys --keyid-format LONG
```

### Export private key in gpg

```
gpg2 --export-secret-key -a "your_username"
```

### Export public key in gpg
your_key_id is the HASH id in front of `sec` in previous command.

```
gpg2 --armor --export your_key_id
```

### Set a pgp key for git

```
git config --global user.signingkey your_key_id
```

## SSH

### Generate key

```
ssh-keygen -t rsa -b 4096 -C "dylanrichardson1996@gmail.com"
```


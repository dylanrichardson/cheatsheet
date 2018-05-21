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
gpg --gen-key
```

### Check current keys

```
gpg --list-secret-keys --keyid-format LONG
```

### Export private key in gpg

```
gpg --export-secret-key -a "your_username"
```

### Export public key in gpg
your_key_id is the HASH id in front of `sec` in previous command.

```
gpg --armor --export your_key_id
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


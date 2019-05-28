# tell
Tell is a light tool to ease the automated install of our Macbooks.

This playbook installs and configures most of the software we use on our Macbooks for web and software development.

## Origin of the name
[Wiliam Tells](https://en.wikipedia.org/wiki/William_Tell) story of Shooting an apple off one's child's head.

## Shoot the arrow
1. Clone/download this repository to your local drive.
1. Run `$ ./tell` inside this directory.


## Manual tasks and known bugs
### Permission error while installing zsh
```
sudo chgrp -R staff ~/.antigen
sudo chgrp staff ~/.zshrc
chsh -s /bin/zsh
```

### Set your prefered font in your terminal
@see https://github.com/viasite-ansible/ansible-role-zsh#configure-terminal-application

### Install ttmp32gme
[Download ttmp32gme](https://github.com/thawn/ttmp32gme)

### Install Fonts
...

### Set up cloud drives
- box-sync
- google drive
- ownCloud
- iCloud

## Kudos
Originally inspired by [superlumic/superlumic](https://github.com/superlumic/superlumic) and [geerlingguy/mac-dev-playbook](https://github.com/geerlingguy/mac-dev-playbook).

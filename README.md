# tell
Tell is a light tool to ease the automated install of our Macbooks.

This playbook installs and configures most of the software we use on our Macbooks for web and software development.

## Origin of the name
[Wiliam Tells](https://en.wikipedia.org/wiki/William_Tell) story of Shooting an apple off one's child's head.

## Shoot the arrow
1. Clone/download this repository to your local drive.
1. Run `$ ./tell` inside this directory.


## Running a specific set of tagged tasks
You can filter which part of the provisioning process to run by specifying a set of tags using ansible-playbook's --tags flag. The tags available are dotfiles, homebrew, mas, extra-packages and osx.
```sh
ansible-playbook main.yml -K --tags "dotfiles,homebrew"
```

## Manual tasks and known bugs
### Permission error while installing zsh
```sh
sudo chgrp -R "LL\Domain Users" ~/.antigen
sudo chgrp "LL\Domain Users" ~/.zshrc
chsh -s /bin/zsh
```

### Fix annoying error in zsh
In ~/.zshrc
```sh
# alias fd=fdfind # for correct working of sorenson-axial/fzf-widgets auskommentieren
```

### Install ttmp32gme
[Download ttmp32gme](https://github.com/thawn/ttmp32gme)

### Install helpful apps
- <https://apps.apple.com/us/developer/sindre-sorhus/id328077650>

### Set up cloud drives
- box-sync
- google drive

## Kudos
Originally inspired by [superlumic/superlumic](https://github.com/superlumic/superlumic) and [geerlingguy/mac-dev-playbook](https://github.com/geerlingguy/mac-dev-playbook).
<https://github.com/lafarer/ansible-role-osx-defaults> and <https://gist.github.com/vraravam/5e28ca1720c9dddacdc0e6db61e093fe> for osx-defaults in a very structured way.

<https://macos-defaults.com/menubar/dateformat.html>
<https://ansible.fontein.de/collections/community/general/osx_defaults_module.html>
<https://coderwall.com/p/gfmwlw/fixing-arrow-keys-in-iterm-2>

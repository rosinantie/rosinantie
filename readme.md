my developer tools

# terminal

iterm2 or terminal with fish(oh-my-fish) deafult theme

## theme setup

/Users/annz/.config/fish/config.fish

set -x LSCOLORS 'ExFxBxDxCxegedabagacad'

set -g fish_greeting (printf '\e[92mWelcome, Dilip!\e[0m')

## git setup

### command :

gitk

# VS CODE

FONT - Operator Mono

THEME - Operator Mono Theme(extension)

---

# SETUPING TWO ACCOUNT ONE FOR WORK AND ANOTHER FOR PERSONAL

1.create .ssh

2.create a ssh key gen using with your email then

ssh-keygen -t ed25519 -C "[your_email@example.com](mailto:your_email@example.com)" -f ~/.ssh/id_rsa_personal

the above command will generate a ssh-keygen with id_rsa_personal this file name

3.copy the pub file

something like this:

ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIL4Wdtx7fuO2sAWU/JK7/W/hYS+a+pbfkMgfj1ryqDCh [your_email@example.com](mailto:your_email@example.com)

4.setuping git for cloning form the repository

```markdown
# Account 1

Host github.com-personal
HostName github.com
User git
IdentityFile ~/.ssh/id_rsa_personal

# Account 2

Host github.com-office
HostName github.com
User git
IdentityFile ~/.ssh/id_rsa_office
```

4.in .gitconfig

```
[alias]
	ci-personal = "!f() { git config user.name 'dilipgonadev'; git config user.email 'dilipgona.dev@gmail.com'; }; f"
	ci-office = "!f() { git config user.name 'dilipannztech'; git config user.email 'dilip@annztech.com';}; f"
```

got to. command line and command git ci-personal to change the name and email

for example

if your now working in office then use **ci-office**

if your working in your personal then use **ci-personal**

---

```sh
# Setup SSH

ls -al ~/.ssh

# create new ssh
ssh-keygen -t ed25519 -C "srilatha@pc"

# list files to see if ssh file is created
ls -al ~/.ssh

# update config file
echo "
Host github.com
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519" >> ~/.ssh/config

# open this github link
https://github.com/settings/keys

## copy all the string by selecting
cat ~/.ssh/id_ed25519.pub
```

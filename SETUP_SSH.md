# Setup SSH on MAC

```sh
ls -al ~/.ssh
# create new ssh
ssh-keygen -t ed25519 -C "megha@mac"


# list files to see if ssh file is created
ls -al ~/.ssh
# output the new ssh files
# id_ed25519
# id_ed25519.pub

# check
eval "$(ssh-agent -s)"

# update config file
echo "
Host github.com
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519" >> ~/.ssh/config

# check the file content
cat ~/.ssh/config

# if ssh password is set then us the following
ssh-add --apple-use-keychain ~/.ssh/id_ed25519

# copy the ssh public key to clipboard
pbcopy < ~/.ssh/id_ed25519.pub

# open this github link

https://github.com/settings/keys

# copy
pbcopy < ~/.ssh/id_ed25519.pub

```

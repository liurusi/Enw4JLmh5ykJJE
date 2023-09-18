## Goal:
### Avoid being asked to input a password every time I push my repo.


## Steps:
### 1. Generate a new ssh key pair. Use your own email addr inside " "

```
ssh-keygen -t ed25519 -C "your@email.addr"
```

### 2. Assure ssh-agent is watching.

```
eval "$(ssh-agent -s)"
```

### 3. Add new_key locally
```
ssh-add new_key
```

### 4. Copy new_key.pub in clipboard.
```
wl-copy < new_key.pub 
```

### 5. Open github.com, and find SSH and GPG Key in Setting. Then click add new ssh key, Enter the name "lt" and paste the pub key into the key input frame.


### 6. Switch the repo from https to ssh. use specific owner and repo.
```
git remote set-url origin git@github.com:owner/repo.git 
```


### 7. Done.
```
git remote -v
git status
git push
```

## Goal:
### Avoid being asked input password every time push my reop.


## Steps:
### 1. Generate a new ssh key pair.

```
ssh-keygen -t ed25519 -C "liurusi@163.com"
```

### 2. Assure ssh-agent is watching.

```
eval "$(ssh-agent -s)"
```

### 3. Add new_key localy
```
ssh-add liurusi@github 
```

### 4. Copy new_key.pub in clipboard.
```
wl-copy < cat liurusi@github.pub 
```

### 5. Open github.com, find SSH and GPG Key in Setting. Then click add new ssh key, Enter name "lt" and paste the pub key into the key input frame.


### 6. Switch the repo from https to ssh
```
git remote set-url origin git@github.com:liurusi/Enw4JLmh5ykJJE.git 
```


### 7. Done.
```
git remote -v
git status
git push
```

## Create a branch and choose it
```bash
git checkout -b "BRANCH_NAME"
```

## Attach project to git remote
```bash
git init
git add .
git commit -m "Init"
git remote add origin PROJECT_URL
git push -u -f origin master
```

## Pull with target shh key
```bash
GIT_SSH_COMMAND='ssh -i PATH_TO_KEY -o IdentitiesOnly=yes' git pull
```

## Remove files from git history
```bash
git filter-branch --tree-filter 'rm -f <path_to_file>' HEAD
git push origin --force --all
```

## Reset branch with remote changes
```bash
git fetch --all
git branch backup-master
git reset --hard origin/master
```

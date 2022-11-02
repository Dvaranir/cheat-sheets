## Create a branch and choose it
```bash
git checkout -b "branch name"
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
ssh -i /home/shop/.ssh/itsupport_git -o IdentitiesOnly=yes' git pull
```

## Reset local project with remote changes
```bash
git fetch
git reset --hard
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

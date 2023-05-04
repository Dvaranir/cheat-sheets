## Create user
```bash
sudo adduser username
```

## Add user to group
```bash
sudo usermod -aG groupname username
```

## Log as user
```bash
su - username
```

## Add user to sudo
```bash
sudo usermod -aG sudo myuser
```

## Change user's password
```bash
passwd username
```

## Reload shell
```bash
source ~/.bashrc
```
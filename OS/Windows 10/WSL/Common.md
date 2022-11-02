## .bashrc location - it's named as bash.bashrc
```
/etc
```

## Remove distro
```bash
wsl --unregister
```

## Cloning a WSL distro

### Firstly you must export the WSL distribution you wish to clone.
```bash
wsl.exe --export ORIGINAL_DISTRIBUTION_NAME FILE_NAME
```
**ORIGINAL_DISTRIBUTION_NAME** is the name of the distribution you wish to export.

**FILE_NAME** is the full path to a tar file that will be created.

### Secondly you must now import the distribution you just cloned with the following command:
```bash
wsl.exe --import NEW_DISTRIBUTION_NAME INSTALL_LOCATION FILE_NAME
```

**NEW_DISTRIBUTION_NAME** is the name of the new distribution that will be created.

**INSTALL_LOCATION** is path to the folder the distribution will be installed to.

**FILE_NAME** is the full path file to the tar file you created in the previous step.

### Now you can start the cloned distribution by running the following command:
```bash
wsl --distribution NEW_DISTRIBUTION_NAME
```

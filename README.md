# apt-repo
This experimnetal repo contains the Open Source Components used to build a Monroe Node (Debian stretch)

## To add the repository to a system/node 
As this is a experimental repo the packages are not signed and we muts tell apt to trust the repo by add ing the switch ```[trusted=yes]```

### add the repo:
```echo 'deb [trusted=yes] https://raw.githubusercontent.com/MONROE-PROJECT/apt-repo/master stretch main' > /etc/apt/sources.list.d/monroe.list```

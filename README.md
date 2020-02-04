# dev-tools

A set of useful stuff for daily use for development purposes

# Git

## Remove local tracked branches that's removed on remote
```sh
git fetch -p && for branch in `git branch -vv | grep ': gone]' | awk '{print $1}'`; do git branch -D $branch; done
```
```

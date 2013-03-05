---
layout: post
title: "Installing git autocompletion script for mac"
date: 2013-02-22 11:57
comments: true
categories: [git, mac]
---
```bash
curl https://raw.github.com/git/git/master/contrib/completion/git-completion.bash -o ~/.git-completion.bash
```
No need to worry about what directory you're in when you run this command, it is set to go to your home directory as ~ is used with the target.

Then I added to my ~/.bash_profile file the following 'execute if it exists' code:
```bash
if [ -f ~/.git-completion.bash ]; then
  . ~/.git-completion.bash
fi
```

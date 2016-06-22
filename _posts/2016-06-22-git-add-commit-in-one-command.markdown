---
published: true
title: Git add & commit in one command
layout: post
---
I would like to share a small tip to commit your working code more quickly.

Normally, when I want to commit my code I need at least `2 commands`:

    git add -A
    git commit -m "message"

Now I found another way to archive the same result by just `1 command`

### Create an alias

    git config --global alias.ac '!git add -A && git commit'

### Usage

    git ac -m "message"

Thank you for reading
---
layout: post
section-type: post
title: Start Genymotion player from Command line
category: Genymotion
tags: [ 'genymotion', 'android' ]
---

I am very lazy. So, I am trying to use Keyboard to replace Mouse clicks as many as possible. But, open Genymotion player always take me a lot of clicks. I am not happy with that.

## Professional way

Cmd + Space (Spotlight) -> "Genymotion" -> (Wait a moment) click "play" button. **DONE**

Not too much, right? But, like I said: "I am very lazy". So, I can not do that everyday.

## Lazy way
### 1. Find the player's vmid

```
# First, get a list of the VM's you have installed
VBoxManage list vms

# Returns something like "5.0.0 - API 21 - 768x1280" {091d022d-6a7b-4475-845f-7a6e06024fb6}
```

Copy the VM ID, e.g. `091d022d-6a7b-4475-845f-7a6e06024fb6`

### 2. Scripting

Create a shell script file: `geny5.sh` with the content below: 

```
# Launch a specific VM
open -a /Applications/Genymotion.app/Contents/MacOS/player.app --args --vm-name '091d022d-6a7b-4475-845f-7a6e06024fb6'
```

### 3. Use

My day was saved by the following command:

```
sh [path to geny5.sh]
```

## Lord of lazier way

### 1. Alias

Add following line to `~/.bash_profile`:

```
alias geny5="open -a /Applications/Genymotion.app/Contents/MacOS/player.app --args --vm-name '091d022d-6a7b-4475-845f-7a6e06024fb6'"
```

Run `source` command to apply change.

```
source ~/.bash_profile
```

### 2. Enjoy
    
What's `geny5.sh`. I just `geny5` ^^.

```
geny5
```


**Welcome to Lazier Group** 
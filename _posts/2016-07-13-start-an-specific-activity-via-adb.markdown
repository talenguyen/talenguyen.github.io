---
layout: post
section-type: post
title: Start an activity from command-line via adb
category: Git
publish: false
tags: [ 'adb', 'commandline', 'activity' ]
---

I would like to share a small tip to commit your working code more quickly.

## Problem

Normally, when I want to commit my code I need at least `2 commands`:

## Start an activity

    adb shell am start -a android.intent.action.MAIN -n com.XXX.xxx/com.XXX.xxx.Main --es STRING_PAR_NAME stringParameterValue

## What about parameters?

    [-e|--es <EXTRA_KEY> <EXTRA_STRING_VALUE> ...]
    [--esn <EXTRA_KEY> ...]
    [--ez <EXTRA_KEY> <EXTRA_BOOLEAN_VALUE> ...]
    [--ei <EXTRA_KEY> <EXTRA_INT_VALUE> ...]
    [--el <EXTRA_KEY> <EXTRA_LONG_VALUE> ...]
    [--eu <EXTRA_KEY> <EXTRA_URI_VALUE> ...]
    [--eia <EXTRA_KEY> <EXTRA_INT_VALUE>[,<EXTRA_INT_VALUE...]]
    [--ela <EXTRA_KEY> <EXTRA_LONG_VALUE>[,<EXTRA_LONG_VALUE...]]

    adb shell am start -a android.intent.action.MAIN -n com.XXX.xxx/com.XXX.xxx.Main --es STRING_PAR_NAME stringParameterValue

Thank you for reading
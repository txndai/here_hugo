---
title: "Nvm"
date: 2022-04-04T13:53:48+02:00
description: 
tags: [resource]
---

## Output I got after install
Talking about globally installed modules, too lazy to look into all this now;) But it may be handy later

```bash
=> You currently have modules installed globally with `npm`. These will no
=> longer be linked to the active version of Node when you install a new node
=> with `nvm`; and they may (depending on how you construct your `$PATH`)
=> override the binaries of modules installed with `nvm`:

/opt/homebrew/lib
├── @aws-amplify/cli@7.6.22
=> If you wish to uninstall them at a later point (or re-install them under your
=> `nvm` Nodes), you can remove them from the system Node as follows:

     $ nvm use system
     $ npm uninstall -g a_module
```

## Installed nvm but terminal isn't picking it up

Add this to your `.zshrc`
```
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```
- [read more here](https://github.com/nvm-sh/nvm/blob/master/README.md#troubleshooting-on-macos)
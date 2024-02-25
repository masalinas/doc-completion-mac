## Description
Add completion script for a CLI in mac with zsh shell and oh-my-zsh extension. In our case we will configure Argo CLI completion.

## Step 01
First create the completion zsh script to be used for your CLI like this:

```sh
$ argo completion zsh > argo-workflows.plugin.zsh
```

## Step 02
Create a folder inside custom plugins of oh-my-zsh to load this completion by zsh shell

```sh
$ cd ~/.oh-my-zsh/custom/plugins
$ mkdir argo-workflows
$ mv argo-workflows.plugin.zsh ~/.oh-my-zsh/custom/plugins/argo-workflows
```

## Step 03
Activate this plugin in the **.zshrc** file

```sh
plugins=(git docker docker-compose kubectl helm terraform vault vagrant azure aws argo-workflows)
```

## Step 04
Reload zsh again

```sh
$ source .zshrc
```

## Description
Add completion script for a CLI in mac with zsh shell and oh-my-zsh extension. In our case we will configure Argo CLI completion.

## Step 01
First create the completion zsh script with a name to be used for your CLI like this:

```sh
$ argo completion zsh > argo-workflows.plugin.zsh
```

## Step 02
Create a folder with the same name as the zsh plugin script inside custom plugins of oh-my-zsh to load this completion by zsh shell script like this: 

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

## Step 05
Use the autocompletion form your CLI with the TAB key

```sh
$ argo
archive           -- manage the workflow archive
auth              -- manage authentication settings
cluster-template  -- manipulate cluster workflow templates
completion        -- output shell completion code for the specified shell (bash or zsh)
cp                -- copy artifacts from workflow
cron              -- manage cron workflows
delete            -- delete workflows
executor-plugin   -- manage executor plugins
get               -- display details about a workflow
help              -- Help about any command
lint              -- validate files or directories of manifests
list              -- list workflows
logs              -- view logs of a pod or workflow
node              -- perform action on a node in a workflow
resubmit          -- resubmit one or more workflows
resume            -- resume zero or more workflows (opposite of suspend)
retry             -- retry zero or more workflows
server            -- start the Argo Server
stop              -- stop zero or more workflows allowing all exit handlers to run
submit            -- submit a workflow
suspend           -- suspend zero or more workflows (opposite of resume)
template          -- manipulate workflow templates
terminate         -- terminate zero or more workflows immediately
version           -- print version information
wait              -- waits for workflows to complete
watch             -- watch a workflow until it completes
```

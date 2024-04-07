## Install

Install **git** using [homebrew](../../mac/homebrew/index.md) with the following command:

```shell
brew install git
```

## Configuration

### Set username
```shell
git config --global user.name "[Firstname Lastname]"
```

### Set email

```shell
git config --global user.email "[EmailId]"
```

### Set credential helper

```shell
git config --global credential.helper store
```

This will store your credentials in a plain text file at `~/.git-credentials`.

## Usage

### Init

Initialize got tracking inside current directory

```shell
git init
```

Initialize git tracking inside a new directory

```shell
git init [directory]
```

### Clone

Clone a repository

```shell
git clone [url]
```

Clone only a specific branch

```shell
git clone --branch [branch] [url]
```

Clone a repository to a specific directory

```shell
git clone [url] [directory]
```

### Branch

Create a new branch

```shell
git branch [branch]
```

Create a new branch and switch to it

```shell
git checkout -b [branch]
```

Switch to a branch

```shell
git checkout [branch]
```

Delete a branch

```shell
git branch -d [branch]
```

Delete a branch forcefully

```shell
git branch -D [branch]
```

Merge a branch

```shell
git merge [branch]
```

Merge a branch with a message

```shell
git merge [branch] -m "Message"
```


### Add

Add a file to staging area

```shell
git add [file]
```

Add all files to staging area

```shell
git add .
```

Stage all files except a specific file

```shell
git add -u
git git reset HEAD main/dontcheckmein.txt #or
git restore --staged main/dontcheckmein.txt
```

Remove a file from staging area

```shell
git rm [file]
```

### Commit

See the changes in the staging area

```shell
git status
```

Saving the staged changes with a message

```shell
git commit -m "Message"
```

Saving the staged changes with a message and adding all changes

```shell
git commit -am "Message"
```

Edit the last commit message

```shell
git commit --amend -m "New Message"
```

### Saving

Saving stage and unstaged changes

```shell
git stash
```

Saving stage and unstaged changes with a message

```shell
git stash save "Message"
```

Saving stage and unstaged changes with a message and include untracked files

```shell
git stash -u save "Message"
```

Apply the last stash

```shell
git stash apply
```

Apply a specific stash

```shell
git stash apply stash@{n}
```

Apply the last stash and remove it from the list

```shell
git stash pop
```

Remove the last stash

```shell
git stash drop
```

Remove a specific stash

```shell
git stash drop stash@{n}
```

### Diff

See the changes between the working directory and the staging area

```shell
git diff
```

See the changes between 2 commits

```shell
git diff [commit1] [commit2]
```

### Push to a previous commit

There are 2 ways of doing this

#### Reset 

!!! Warning "Use with caution"
    Use this wisely as this would manipulate the git history and could very well jeopardise everything for you.

```shell
git reset [commitId] --hard && git push --force
```

- `--soft` - Moves the HEAD to the commitId and keeps the changes in the staging area
- `--mixed` - Moves the HEAD to the commitId and keeps the changes in the working directory
- `--hard` - Moves the HEAD to the commitId and discards all changes
- `--merge` - Moves the HEAD to the commitId and keeps the changes in the staging area and working directory
- `--keep` - Moves the HEAD to the commitId and keeps the changes in the working directory

???info "Read more"
    [Simon Dosda's Post](https://simondosda.github.io/posts/2022-01-04-git-reset.html)

#### Revert

```shell
git revert --no-commit [commitId1 commitId2] && git push
```

## GitHub via SSH

[Generate a new SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key)

```shell
ssh-keygen -t ed25519 -C "[EMAIL ID]"
```

[Add SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account)


## Cheat Sheet

[Download Cheat Sheet](./downloads/git-cheat-sheet-education.pdf){:download="git-cheat-sheet-education.pdf"}

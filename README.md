# `dug`

This program displays the content of a private repository's folder in Github, and lets you choose one folder to download. It also allows you to merge it using [cylf](https://github.com/the-other-mariana/cylf), in case the folder contains parts of a larger file.

## Set Up

1. Make sure you have `cylf` in your PATH by typing:

```
export PATH="${HOME}/Documents/github-mariana/cylf/bin/ubuntu:${PATH}"
```

either in your `~/.bashrc` file or in a terminal.

2. Fill up the `.env` variables:

```
GITHUB_ACCESS_TOKEN=[YOUR_GITHUB_ACCESS_TOKEN]
GITHUB_USER=user_name
GITHUB_REPOSITORY=repo_name
REPO_PATH=some_repo_folder
REPO_BRANCH=master
MERGE_EXTENSION=[mp4 | mp3 | py | pdf | ...]
```

3. Run dug:

- Linux (Ubuntu 20.04 LTS - tested)

```
sudo chmod 777 dug
./dug
```

- Windows 10

```
start dug.exe
```

- Source code

You must have installed Golang version `go1.18.7 linux/amd64` and then type:

```
export GO111MODULE=off
go run dug.go
```


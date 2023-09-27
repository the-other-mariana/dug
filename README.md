# `dug`

This program displays the content of a private repository's folder in Github, and lets you choose one folder to download. It also allows you to merge it using [cylf](https://github.com/the-other-mariana/cylf), in case the folder contains parts of a larger file.

## Set Up

1. Make sure you have `cylf` in your PATH by typing:

```
export PATH="<Path/to/cylf/bin/ubuntu>:${PATH}"
```

either in your `~/.bashrc` file or in a terminal right before running Dug. For example: 

```
export PATH="/home/mariana/go/src/github.com/the-other-mariana/cylf/bin/ubuntu:$PATH"
```

This will allow the Dug program to call `cylf` instead of `./cylf`

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
export PATH="<Path/to/cylf/bin/ubuntu>:${PATH}"
go mod init
go build dug.go
./dug
```

### To Cross Compile The Source Code

- Windows 10

```
GOOS=windows GOARCH=amd64 go build dug.go
```

- Raspberry Pi 3 Model B

```
GOOS=linux GOARCH=arm go build dug.go
```


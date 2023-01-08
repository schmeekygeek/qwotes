# Qwote

A simple Bash script to show qwotes on terminal startup... or anywhere :)

## Dependencies
- `jq` Command line JSON parser.
- `curl` (why did I even bother writing this lol)

## Installation
Make the script executable and place it anywhere in your `PATH`

```bash
$ git clone https://github.com/schmeekygeek/qwote.git
$ cd qwotes
$ chmod +x qwotes
$ cp qwotes ~/.local/bin/
```

## Usage
- Place this somewhere you like in your `.bashrc`
```
RED='\033[0;31m'
BLUE='\033[0;34m'
NC='\033[0m'
echo
echo -en "${RED}\e[3m❤ $(cat ~/.cache/qwote.txt) ❤\e[0m${NC}"
echo -en "\n${BLUE}\e[3m- $(cat ~/.cache/author.txt)\e[0m${NC}"
echo
```

- Then do,
```bash
$ qwotes
Generating qwote...
Successfully generated qwote!
```

Your qwote should be visible now.

> For a new qwote, simply run `qwotes` again and refresh your terminal:
```bash
$ qwotes && clear && source ~/.bashrc
```

## Uninstalling
Remove the script from the `PATH`

```bash
$ rm ~/.local/bin/qwotes
```

## Credits
- [api.quotable.io](https://api.quotable.io) The API

<p align="center"><img src="https://img.shields.io/static/v1.svg?style=for-the-badge&label=License&message=GPL&logoColor=d9e0ee&colorA=302d41&colorB=c9cbff"/></a></p>

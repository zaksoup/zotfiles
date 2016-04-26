# Dotfiles

This repo contains three things:

1. dotfiles (.zshrc, etc)
1. scripts to install said dotfiles and their possible prerequisites (oh-my-zsh)
1. instructions for how to consume the above 2 things

## Usage

For best results, install while listening to
[The Cowboy Bebop OST](https://itunes.apple.com/us/album/cowboy-bebop-original-soundtrack/id489780131)

### Prerequisites

These dotfiles work best when dependencies are installed with brew wherever possible,
`*` indicates the dependency is not available via brew.

* xcode CLI tools (`xcode-select --install`) *
* [homebrew](http://brew.sh)

*Notes on ZSH*: these dotfiles assume that your shell is ZSH. While you can install
them on a machine for which the primary login shell is `bash` they specifically target
oh-my-zsh and zsh by installing a `.zshrc` file and omz themes. Furthermore, the shebang
of all scripts in this repo is `#!/bin/zsh`. Nothing will run without zsh installed.

### Installation

It is best to assume that the following paths are required as is unless a specific
exception is noted.

1. clone dotfiles:

    ```bash
    git clone git@github.com:zaksoup/dotfiles.git ~/workspace/dotfiles
    ```
1. run install script

    ```bash
    cd ~/workspace/dotfiles
    ./install
    ```

The install script will:

* install git via brew
* install the [git-duet](https://github.com/git-duet/git-duet) brew package
* golang 1.6 via brew
* iterm2 via `brew cask`
* [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) *
* clone and install [powerline fonts](https://github.com/powerline/fonts)
* add `git ci` as an alias for `git duet-commit`
* overwrite the current `~/.zshrc` with one from this repo
* install the "Zagnoster" ZSH theme (agnoster with git-duet support)
* download and install the [Hybrid colorscheme](https://github.com/w0ng/vim-hybrid) for iTerm

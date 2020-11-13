# easyjump.tmux

EasyMotion for Tmux

## Requirements

- Python >= 3.8

## Installation

- [TPM](https://github.com/tmux-plugins/tpm)

  1. Add to `~/.tmux.conf`:

     ```tmux
     set-option -g @plugin "roy2220/easyjump.tmux"
     ```

  2. Press `prefix` + <kbd>I</kbd> to install the plugin.

- Manual

  1. Fetch the source:

     ```sh
     git clone https://github.com/roy2220/easyjump.tmux.git /PATH/TO/DIR
     ```

  2. Add to `~/.tmux.conf`:

     ```tmux
     run-shell "/PATH/TO/DIR/easyjump.tmux"
     ```

  3. Reload Tmux configuration:

     ```sh
     tmux source ~/.tmux.conf
     ```

## Usage

Press `prefix` + <kbd>j</kbd>

## Configuration

```tmux
# defaults:
set-option -g @easyjump-key-binding "j"
set-option -g @easyjump-label-chars "fjdkslaghrueiwoqptyvncmxzb1234567890"
set-option -g @easyjump-label-attrs "\e[1m\e[38;5;172m"
set-option -g @easyjump-text-attrs "\e[0m\e[38;5;237m"
set-option -g @easyjump-smart-case "on"
```

## Demonstration

https://asciinema.org/a/372086

**This project is heavily inspired by [tmux-jump](https://github.com/schasse/tmux-jump)**.

There some differences between `tmux-jump` and `easyjump.tmux`:

- `tmux-jump` searches by 1 char and `easyjump.tmux` does by 2 chars.
- `tmux-jump` only matches the prefixes of words, `easyjump.tmux` matches all.
- `tmux-jump` is implemented in Ruby and `easyjump.tmux` is done in Python 3.
- `easyjump.tmux` supports the smart case-insensitive search (turned on by default).

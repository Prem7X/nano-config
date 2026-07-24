# My Ultimate Nano Configuration

This is my custom `~/.nanorc` configuration that upgrades GNU nano with modern text editor features, UI improvements, and safety backups.

## Installation
Copy the text block below and paste it directly into your `~/.nanorc` file. Make sure to run `mkdir -p ~/.nano-backups` in your terminal so the backup feature works!

## The Configuration
```text
# === Basic Editor Features ===
set linenumbers
set mouse
set autoindent
set tabsize 4
set tabstospaces
set softwrap
set indicator
set matchbrackets "(<[{)>]}"
set historylog
set positionlog

# === Modern UI & Behavior ===
set zap
set smarthome
set cutfromcursor
set multibuffer
set minibar

# === Safety & Backups ===
set backup
set backupdir "~/.nano-backups"

# === Writing & Navigation ===
set wordbounds
set atblanks

# === Syntax Highlighting ===
include "/usr/share/nano/*.nanorc"



```markdown
# Nano Configuration

This is a custom `~/.nanorc` configuration that upgrades GNU nano with modern text editor features, UI improvements, and safety backups.

## Installation
1. Open your terminal and create a directory for your backups:
   ```bash
   mkdir -p ~/.nano-backups

```

2. Open your configuration file:
```bash
nano ~/.nanorc

```


3. Paste the configuration block below into the file.

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

```

## How to Save and Exit

1. Press `Ctrl + O` to save the file.
2. Press `Enter` to confirm the file name.
3. Press `Ctrl + X` to exit the editor.

```

```

### Basic Editor Features

* **`set linenumbers`**: Displays a permanent column of line numbers on the left side of the screen.
* **`set mouse`**: Enables mouse support, allowing you to click anywhere to move your cursor or drag to highlight text.
* **`set autoindent`**: When you press Enter, the new line will automatically match the indentation (spaces/tabs) of the previous line.
* **`set tabsize 4`**: Sets the visual width of a tab to exactly 4 spaces (the standard for most programming languages).
* **`set tabstospaces`**: Converts your tab key presses into actual spaces. This prevents code alignment from looking broken when someone opens your file in a different editor.
* **`set softwrap`**: Prevents long lines of text from disappearing off the right edge of the screen by wrapping them visually to the next line.
* **`set indicator`**: Adds a visual scrollbar on the right side of the screen so you know your position in long files.
* **`set matchbrackets "(<[{)>]}"`**: When you place your cursor on an opening bracket like `{` or `(`, it will automatically highlight the closing bracket `}` or `)`.
* **`set historylog`**: Remembers your search and replace history even after you close the editor.
* **`set positionlog`**: Remembers exactly what line your cursor was on when you last closed a file, and puts you right back there when you reopen it.

### Modern UI & Behavior

* **`set zap`**: Allows you to highlight text and instantly delete it by pressing `Backspace` or `Delete` (normally, Nano ignores highlighted selections when you press backspace).
* **`set smarthome`**: Makes the `Home` key smarter. Pressing it once jumps the cursor to the first actual word on the line. Pressing it twice jumps to the absolute left edge of the screen.
* **`set cutfromcursor`**: Changes the `Ctrl + K` (Cut) shortcut so it only cuts the text from wherever your cursor currently is to the end of the line, rather than deleting the entire line.
* **`set multibuffer`**: Allows you to open multiple files at the same time and switch between them using `Alt + <` and `Alt + >`.
* **`set minibar`**: Removes the bulky, two-line shortcut help menu at the bottom of the screen and replaces it with a single, sleek status bar, giving you more screen space to read code.

### Safety & Backups

* **`set backup`**: Every time you save a file, Nano creates a backup of the *previous* version just in case you make a mistake and need to undo it.
* **`set backupdir "~/.nano-backups"`**: Forces all of those backup files to be saved silently in a hidden folder, rather than cluttering up your actual project folders.

### Writing & Navigation

* **`set wordbounds`**: Improves jumping word-by-word (`Ctrl + Left/Right Arrow`) so the cursor properly stops at punctuation marks and symbols, instead of skipping over them.
* **`set atblanks`**: Works together with `softwrap`. It ensures that when a long line wraps to the next line, it breaks cleanly at a space between words, rather than chopping a word right in half.

### Syntax Highlighting

* **`include "/usr/share/nano/*.nanorc"`**: Tells Nano to look in your system's default directory and load the color-coding rules for all standard programming languages (like HTML, Python, bash, etc.).

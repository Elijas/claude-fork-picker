# claude-fork

TUI picker to fork Claude Code sessions from the current directory.

Better UX than the built-in session picker:
- **Searchable** - fuzzy search through recent messages
- **Preview pane** - see conversation history before selecting
- **Sorted by recency** - most recent sessions at the top

## Usage

```bash
claude-fork                    # Pick and fork a session
claude-fork --model sonnet     # Fork with specific model
```

## Install

```bash
# Clone and add to PATH
git clone https://github.com/Elijas/claude-fork-picker.git
export PATH="$PATH:$PWD/claude-fork-picker"

# Or just copy the script
curl -O https://raw.githubusercontent.com/Elijas/claude-fork-picker/main/claude-fork
chmod +x claude-fork
```

## Requirements

- [Claude Code](https://github.com/anthropics/claude-code)
- fzf
- python3

## How it works

1. Finds all sessions for your current working directory
2. Shows them in fzf sorted by recency with a preview pane
3. Forks the selected session with `claude --fork-session --resume <uuid>`

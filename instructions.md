# Instructions — How Everything Works

Hi! This file explains everything you need to know. No tech background required.

---

## Big Picture — What Is All This?

### What is this folder?

This folder (`Projects`) is your workspace. Think of it like a filing cabinet — each folder inside it is a separate project (like a separate drawer). You can have as many projects as you want, and they all live here together.

### What is Git?

Git is like a "save history" system for files. You know how Google Docs lets you go back and see older versions of a document? Git does that for entire folders of files.

Every time you make a meaningful change, you "save" it with a short note about what changed. These saves are called **commits**. If something breaks, you can always go back to an earlier save.

Git lives invisibly inside a hidden folder called `.git` — you never need to touch it.

### What is GitHub?

GitHub is a website that stores a copy of your project on the internet. Think of it like Google Drive but specifically designed for projects that use Git.

Why use it?
- **Backup** — if your computer breaks, your work is safe online
- **Access anywhere** — you can see your files from any computer
- **Sharing** — if you ever want to show someone your work, you send them a link

Your projects live at: https://github.com/tartakovsky2006-ctrl

### What are all these files?

| File | What it is |
|------|-----------|
| `instructions.md` | This file! The guide you're reading right now |
| `to_learn.md` | Your personal list of things to learn |
| `CLAUDE.md` | Instructions for Claude (the AI assistant) so it knows how this project works |
| `.gitignore` | A list of files Git should ignore (like temporary junk files). You'll never need to edit this |
| `.gitattributes` | Tells Git how to handle big files (images, videos, PDFs). You'll never need to edit this |

Files and folders that start with a dot (`.`) are hidden by default. That's normal — they're just behind-the-scenes configuration.

### What is a Terminal?

A terminal is a text-based way to talk to your computer. Instead of clicking buttons and icons, you type commands. It looks like a black or white window with text.

You don't need to use the terminal yourself — Claude handles that for you. But if you see references to "running a command" or "the command line," that's what it means.

### What is Code?

Code is just text that tells a computer what to do. It's written in files, just like any document, but instead of being meant for humans to read, it's meant for computers to follow.

Different **programming languages** are like different human languages — they all accomplish similar things but look different. Some common ones you might hear about:
- **Python** — popular, reads almost like English
- **JavaScript** — makes websites interactive
- **HTML/CSS** — defines what websites look like

### What does "build" or "run" mean?

When someone says they "run" code, it means they tell the computer to actually follow the instructions in the code files. When they "build" something, they're turning the code into a finished product (like turning a recipe into a meal).

### How does Claude fit into all this?

Claude (that's me, the AI you're chatting with) acts as your developer. You tell me what you want in plain English, and I:
1. Write the code
2. Organize the files
3. Save everything with Git
4. Push it to GitHub

You don't need to understand any of the technical details. Just describe what you want, and I'll handle the rest.

### Markdown — the format AI uses to communicate

Files ending in `.md` are Markdown files. It's a simple text format with formatting (headings, lists, tables, links). This is the format AI uses for plans, instructions, work logs, and documentation.

In Visual Studio Code, Markdown files have two modes:

- **Preview mode** — nicely formatted text (like reading a web page). Opens by default.
- **Edit mode** — you see the raw markup symbols (`#`, `**`, `-`, etc.). This is where you can change text.

| Action | How |
|---|---|
| Switch to edit mode | **Double-click** on the text |
| Switch back to preview | **Esc** |

Most `.md` files in the project don't need manual editing — AI does it. But if you want to fix something — double-click, edit, Esc.

---

## Getting Started

1. Open **Visual Studio Code**
2. If the project isn't open — drag the `Projects` folder onto the Visual Studio Code window
3. Open the terminal: **Cmd + J**
4. Type the command and press Enter:
   ```
   claude -y -c -b
   ```
5. Chat with Claude right in the terminal — write tasks in plain language

The terminal panel opens instead of the file panel. Want files — pick a file and hide the terminal with Cmd+J. Want the chat — press Cmd+J again.

---

## Visual Studio Code Shortcuts

All shortcuts are for macOS. On Windows/Linux, replace **Cmd** with **Ctrl**.

### Panels and Sidebars

| Action | Keys |
|---|---|
| Open/close **file tree** (left panel) | `Cmd + E` |
| Open/close **right sidebar** | `Cmd + B` |
| Open/close **bottom panel** (terminal = chat with Claude) | `Cmd + J` |
| Create new terminal | `Cmd + T` |

### Search

| Action | Keys |
|---|---|
| Search **in current file** | `Cmd + F` |
| Search **across entire project** | `Cmd + Shift + F` |
| Jump to file by name | `Cmd + P` |
| Open command palette (all VS Code actions) | `Cmd + Shift + P` |

### Files

| Action | Keys |
|---|---|
| Save file | `Cmd + S` |
| Save all files | `Cmd + Option + S` |

### Other

| Action | Keys |
|---|---|
| Increase font size | `Cmd + =` |
| Decrease font size | `Cmd + -` |

---

## Terminal Keyboard Shortcuts

These work in the terminal (the text area where you type commands and chat with Claude). They save you from pressing the arrow key a million times.

All shortcuts are for macOS.

### Moving the Cursor

| What it does | Keys |
|---|---|
| Move **one character** left | `Left arrow` |
| Move **one character** right | `Right arrow` |
| Jump **one word** left | `Option + Left arrow` |
| Jump **one word** right | `Option + Right arrow` |
| Jump to the **beginning** of the line | `Cmd + Left arrow` |
| Jump to the **end** of the line | `Cmd + Right arrow` |

### Deleting Text

| What it does | Keys |
|---|---|
| Delete one character **to the left** (backspace) | `Delete` (backspace key) |
| Delete one **word to the left** | `Option + Delete` |
| Delete **everything to the left** of the cursor (whole line back) | `Cmd + Delete` |

### Controlling What's Running

| What it does | Keys |
|---|---|
| **Cancel** whatever is currently running | `Ctrl + C` (the one Ctrl shortcut you actually need) |
| **Clear** the terminal screen | `Cmd + K` or type `clear` |

### History

| What it does | Keys |
|---|---|
| Previous command | `Up arrow` |
| Next command | `Down arrow` |

### Escape Key in Claude Code

The Escape key does different things depending on what Claude is doing at the moment. Think of it as "go back one step":

| Press # | What's happening | What Escape does |
|---|---|---|
| **1st** press | Claude is working (running code, writing files) | **Stops** Claude mid-action |
| **2nd** press | You have text typed in the input box | **Clears** the input box |
| **3rd** press | Input is already empty | **Goes back** to your previous message so you can edit and resend it |

---

## Launching Claude in the Terminal

Claude is launched by typing a command in the VS Code terminal. Open the terminal (`Cmd + J`) and type the command.

### Main Launch Options

| Command | What it does |
|---|---|
| `claude -y` | New conversation with full access to your machine (standard launch) |
| `claude -c -y` | Continue the last conversation |
| `claude -r -y` | Pick which past conversation to continue |
| `claude -b -y` | New conversation with browser access |
| `claude -c -b -y` | Continue last conversation + browser access |

### Flags Explained

- `-y` (or `--yolo`) — gives Claude full access to files and commands. **Always needed.**
- `-c` (or `--continue`) — continue the last conversation (don't start a new one).
- `-r` (or `--resume`) — show a list of past conversations and pick which one to continue.
- `-b` (or `--browser`) — give Claude access to the browser (when you need something done in Chrome).

### Examples

Normal launch (new conversation):
```
claude -y
```

Continue where you left off:
```
claude -c -y
```

Go back to a specific past conversation:
```
claude -r -y
```

Need something in the browser (e.g., check a website):
```
claude -b -y
```

Continue a past conversation and give browser access:
```
claude -c -b -y
```

---

## Chatting with Claude in the Terminal

| Action | How |
|---|---|
| Send a message | **Enter** |
| New line (without sending) | **Shift + Enter** |
| Paste a screenshot or image | **Cmd + V** (just copy an image and paste it into the chat) |
| Attach a file | Drag a file from the file tree directly into the terminal |
| Open a link from the terminal | **Cmd + click** on the link |

Dragging files is handy when you want to remind Claude about something specific — like a plan or a past conversation (see below).

---

## The .plans and .worklogs Folders

Every project has two behind-the-scenes folders:

### `.plans/` — Plans

Before changing anything, Claude writes a **plan** — what it's about to do and why. This lets you:
- See what Claude is planning before it starts
- Check if it understood your task correctly

### `.worklogs/` — Work Journal

After finishing work, Claude writes a **worklog** — what exactly was done, what decisions were made, what's left for later. This lets you:
- Remember what happened in past sessions
- Understand the context behind changes

### How to Use Them

- Open the `.plans/` or `.worklogs/` folder in the file tree on the left and click any file to read it.
- To **remind Claude** about a past plan or work — drag the file from the file tree directly into the terminal. Claude will read it and remember the context.
- Files are sorted by date (newest at the bottom). The filename contains the date and a short description.

---

## Tips for Getting Started

1. **Cmd + P** — the most useful shortcut. Start typing a filename, and VS Code will find it for you.
2. **Cmd + Shift + P** — if you don't know how to do something, open the command palette and start typing what you want (e.g., "format", "theme", "font size").
3. The left panel with files is your "explorer." Right-click on a file or folder to see a menu with actions (rename, delete, create new file).

---

*This file will be updated as new things come up. If anything is confusing, just ask!*

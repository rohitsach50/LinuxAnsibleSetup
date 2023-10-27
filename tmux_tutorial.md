---

# Introduction to tmux: A Beginner's Guide

## Introduction

Welcome to the world of `tmux`, an indispensable tool for Linux power users! Tmux stands for "terminal multiplexer", and it allows you to run multiple terminal sessions inside a single window. This tutorial will guide you through the basics of `tmux` so you can make the most of your terminal experience.

## Prerequisites:
- A Linux system or environment.
- Basic knowledge of terminal commands.

## Steps

### Step 1: Installing tmux
1. Open your terminal.
2. Update your package list:
   ```bash
   sudo apt update
   ```
3. Install tmux:
   ```bash
   sudo apt install tmux
   ```

### Step 2: Launching tmux
Type `tmux` and press `Enter`:
```bash
tmux
```
This will start a new `tmux` session, and you might notice a green bar at the bottom of your terminal, which is the `tmux` status bar.

### Step 3: Understanding Basic tmux Key Bindings

Tmux commands are triggered by a combination of a "prefix" key, followed by a command key. By default, the prefix is `Ctrl-b`.

- **Creating a New Window**: Press `Ctrl-b` followed by `c`.
- **Switching Between Windows**: Press `Ctrl-b` followed by a window number (e.g., `0`, `1`, `2`).
- **Splitting Windows (panes)**:
  - **Horizontal Split**: Press `Ctrl-b` followed by `%`.
  - **Vertical Split**: Press `Ctrl-b` followed by `"`.

### Step 4: Navigating Between Panes

- **Move to the Right Pane**: `Ctrl-b` then `Right Arrow`.
- **Move to the Left Pane**: `Ctrl-b` then `Left Arrow`.
- **Move to the Pane Above**: `Ctrl-b` then `Up Arrow`.
- **Move to the Pane Below**: `Ctrl-b` then `Down Arrow`.

### Step 5: Resizing Panes

- **Resize Pane to the Right**: `Ctrl-b` then `Ctrl-Right Arrow`.
- **Resize Pane to the Left**: `Ctrl-b` then `Ctrl-Left Arrow`.
- **Resize Pane Upwards**: `Ctrl-b` then `Ctrl-Up Arrow`.
- **Resize Pane Downwards**: `Ctrl-b` then `Ctrl-Down Arrow`.

### Step 6: Closing Panes and Windows

- **Close Current Pane**: Press `Ctrl-d`.
- **Close Current Window**: Close all panes inside the window or press `Ctrl-b` & `&` and confirm the action.

### Step 7: Detaching and Attaching to tmux Sessions

- **Detach from Current Session**: Press `Ctrl-b` followed by `d`.
- **List Existing Sessions**: In the terminal, type:
  ```bash
  tmux ls
  ```
- **Attach to an Existing Session**: Type:
  ```bash
  tmux attach-session -t [session-name]
  ```

### Step 8: Customizing tmux

Tmux is highly customizable. Your configuration can be saved in a file called `.tmux.conf` in your home directory.

For example, if you want to change the default prefix from `Ctrl-b` to `Ctrl-a`, you can add the following to `.tmux.conf`:
```bash
unbind C-b
set -g prefix C-a
```

### Conclusion:

Congratulations! You've taken your first steps into the powerful world of `tmux`. While we've only scratched the surface, with practice, `tmux` can significantly boost your terminal productivity. Remember, like all tools, the more you use it, the more familiar and comfortable you'll become.

---

This script provides a concise introduction to `tmux` for newcomers. If this is meant for a video or live tutorial, it may be helpful to visually demonstrate each command and its effects, ensuring viewers can understand and replicate each step.
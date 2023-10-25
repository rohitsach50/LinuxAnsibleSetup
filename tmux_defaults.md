In `tmux`, there are default key bindings for most of the operations we discussed. Here they are:

1. **Prefix Key**: The default prefix is `Ctrl-b`. Almost all `tmux` commands are invoked using this prefix, followed by a command key.

2. **Split Panes**:
   - Horizontal split (gives you panes side by side): `Ctrl-b %`
   - Vertical split (gives you panes stacked top to bottom): `Ctrl-b "`

3. **Navigate Panes**:
   - Move to the left pane: `Ctrl-b Left arrow`
   - Move to the right pane: `Ctrl-b Right arrow`
   - Move to the pane above: `Ctrl-b Up arrow`
   - Move to the pane below: `Ctrl-b Down arrow`

4. **Resize Panes**:
   - Resize the current pane left: `Ctrl-b Ctrl-Left arrow`
   - Resize the current pane right: `Ctrl-b Ctrl-Right arrow`
   - Resize the current pane up: `Ctrl-b Ctrl-Up arrow`
   - Resize the current pane down: `Ctrl-b Ctrl-Down arrow`
   
   (Hold down the `Ctrl` key after the prefix to resize in larger steps.)

5. **Switch Windows**:
   - Move to the previous window: `Ctrl-b p`
   - Move to the next window: `Ctrl-b n`

6. **Create New Window**: 
   - `Ctrl-b c`

7. **Close Pane**: 
   - `Ctrl-b x` (It'll prompt you to confirm.)

8. **Close Window**: 
   - Simply close all the panes inside it, and the window will close. Alternatively, if you're in the only pane of a window, `Ctrl-b x` will close the pane and consequently the window. 

9. **Reload Configuration**:
   - There isn't a default binding to reload the configuration, but you can use the command `tmux source-file ~/.tmux.conf` directly in your terminal. Some users set up custom bindings like `Ctrl-b r` for convenience.

It's good to remember these defaults, especially when working on a system that doesn't have a custom `tmux` configuration.
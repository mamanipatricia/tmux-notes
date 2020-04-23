###### tags: `tmux`

TMUX
====
Learning tmux

- **keybind** = combinación de teclas by default bind-key is `Ctrl + b`

## customizing conf of tmux
The conf file is allocated in `~/.tmux.conf` (if the file does't exist you can create it.)

## Commands 
To execute any command in tmux, you have to press the keybind (`ctrl + b`) and then one of the next keys ...

### To manage panels
- To split panel horizontally `%`
- To split panel vertically `"`
- To toggle full screen current panel `z`
- To Move between panels  :arrow_up: :arrow_down: :arrow_left: :arrow_right:
- To highlight numbers of panels `q`
- Para ir a un panel de numero X 
- To go to a number of a panel, `q` then `1` `2` ....`9` 
- To toggle with the last panel `;`

- To show clock :timer_clock: at current panel `t`, press `q` to close the clock.
- To highlight current panel `m`
- To resize panel,  keep pressed `ctrl` and  :arrow_up: :arrow_down: :arrow_left: :arrow_right:
- To move current panel from left to right or from above to below `}`
- To move current panel from right to left or from below to above `{`
**NOTE: This goes clockwise**
 
- To convert current panel to window `!`
- To kill current panel `x`


### To manage window
- To create new window `c` | {1, ..., n} windows
- To switch between windows `0` `1` `2` `3` `....` `9` 
- To change to the next window `n` `n = next`
- To change to the preview window `p` `p =preview`
- To switch between last window `l` `l = last`
- To rename current window `,`
- To kill a window `&`

## To manage Sessions
**Definition of Session:**

A session is a single collection of pseudo terminals under the management of tmux. Each session has one or more windows linked to it. A window occupies the entire screen and may be split into rectangular panes. Any number of tmux instances may connect to the same session, and any number of windows may be present in the same session. Once all sessions are killed, tmux exits.

**Advantages:**
 Tener sesiones para desarrollo y produccion.

- To show all sessions `s`
- To create a new session, you have to be in commandline mode typing `:`  and then write `new`
- To rename current session `$`
- To change next session `)`
- To change previous session `(`
- To detach session `d`

## commands out of tmux
- To list sessions `tmux ls`
- To attach session `tmux a -t <NAME_SESSION>`
- To create a new session`tmux` or `tmux new`
- To kill one session `tmux kill-session -t <NAME_SESSION>`
- to kill all sessions (from server) `tmux kill-server`
- To connect to a session `tmux a -t <NAME_SESSION>` on any terminal, not inside of tmux. `a = attach` `t = target`

- To refresh tmux's configurations without closing tmux `shift + r` or `R`


# ADVANCED so so
## Copy Mode
- To access to copy mode `[`
- To move/scroll on console with large data `ctrl + space`
- To copy data displayed on console .... find out...**(see below)** :point_down: 

## RESOURCES
**Plugins** 
1. To copy and paste data.
https://github.com/tmux-plugins/tmux-yank
2. List all urls showed in terminal 
https://github.com/tmux-plugins/tmux-urlview
3. `tmux-fpp` - a plugin for opening any files on your terminal window
4. `tmux-copycat` - a plugin for regex searches in tmux and fast match selection
5. `tmux-yank` - enables copying highlighted text to system clipboard

**NOTE:**
To install:
1. 
```shell=
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```
2. add plugins into `~/.tmux.conf`
```
# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'

# Other examples:
# set -g @plugin 'github_username/plugin_name'
# set -g @plugin 'git@github.com/user/plugin'
# set -g @plugin 'git@bitbucket.com/user/plugin'
```
3. open tmux
4. press `ctrl + b` (keybind) then `I`, wait a moment to install plugins




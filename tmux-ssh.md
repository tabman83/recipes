tmux-ssh
====
Automatically start tmux on your remote server when ordinarily logging in via SSH (and only SSH)

> Linux, SSH, tmux

To automatically start tmux on your remote server when ordinarily logging in via SSH (and only SSH), 
edit the `~./bashrc` of your user or root (or both) on the remote server accordingly:

```
if [[ -z "$TMUX" ]] && [ "$SSH_CONNECTION" != "" ]; then
    tmux attach-session -t ssh_tmux || tmux new-session -s ssh_tmux
fi
```

This command creates a tmux session called ssh_tmux if none exists, or reattaches to a already existing session with that name.
In case your connection dropped or when you forgot a session weeks ago, every SSH login automatically brings you back to the
tmux-ssh session you left behind.

Source: http://stackoverflow.com/a/40192494/1031228

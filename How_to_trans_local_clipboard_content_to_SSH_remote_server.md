# Goal:
## After copying some text like a URL from Chrome, post this text to a remote SSH server for other commands to use.

```
echo $(ssh 192.168.10.33 wl-paste)
```

## To use this method, the local server needs to run an SSH server and it's running on gnome Wayland.

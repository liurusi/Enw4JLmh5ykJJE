## Goal:
### After copying some text like a URL from Chrome, post this text to a remote SSH server for other commands to use.

# Command:
## Client's WM = Gnome
```
echo $(ssh 192.168.10.33 wl-paste)
```

## PS:
### To use this method, the local machine needs to run an SSH server and it's running on gnome Wayland.


 ## Client's WM = Sway
 ```
 echo $(ssh 192.168.10.33 env WAYLAND_DESKTOP=Wayland-0 wl-paste)
 ```

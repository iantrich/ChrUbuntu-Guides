This will show you how to get the following key bindings

Delete = shift+Backspace
Page Up = shift+Up
Page Down = shift+Down
Home = shift+alt+Up
End = shift+alt+Down
F1 = alt+Back
F2 = alt+Forward
F3 = alt+Reload
F11 = alt+F4
Caps Lock = alt+Search


```
$ sudo apt-get install -y xbindkeys xdotool`
$ sudo nano ~/.xbindkeysrc
```

>"xdotool keyup shift+BackSpace; xdotool key Delete; xdotool keydown shift"
>shift+BackSpace
>"xdotool keyup shift+Up; xdotool key Page_Up; xdotool keydown shift"
>shift+Up
>"xdotool keyup shift+Down; xdotool key Page_Down; xdotool keydown shift"
>shift+Down
>"xdotool keyup shift+alt+Up; xdotool key Home; xdotool keydown shift"
>shift+alt+Down
>"xdotool keyup shift+alt+Down; xdotool key End; xdotool keydown shift"
>shift+alt+Down
>"xdotool keyup alt+XF86Back; xdotool key F1; xdotool keydown alt"
>alt+XF86Back
>"xdotool keyup alt+XF86Forward; xdotool key F2; xdotool keydown alt"
>alt+XF86Forward
>"xdotool keyup alt+XF86Reload; xdotool key F3; xdotool keydown alt"
>alt+XF86Reload
>"xdotool keyup alt+F4; xdotool key F11; xdotool keydown alt"
>alt+F4
>"xdotool keyup alt+XF86Search; xdotool key Caps_Lock; xdotool keydown alt"
>alt+XF86Search


```
$ sudo chmod +x ~/.xbindkeysrc
$ killall xbindkeys
$ xbindkeys &
```




**NOTE:** To find keycodes use the following command:

`$ xev | grep -A2 --line-buffered '^KeyRelease' | sed -n '/keycode /s/^.*keycode \([0-9]*\).* (.*, \(.*\)).*$/\1 \2/p'`

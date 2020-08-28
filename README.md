# sowm (_~~Simple~~ Shitty Opinionated Window Manager_)

<a href="https://user-images.githubusercontent.com/42818929/91505435-dfde8d00-e8cf-11ea-9400-a14acf8f28c5.png"><img src="https://user-images.githubusercontent.com/42818929/91505435-dfde8d00-e8cf-11ea-9400-a14acf8f28c5.png" width="43%" align="right"></a>

An itsy bitsy floating window manager (_420~ sloc! Blaze it_).

- Floating only.
- Fullscreen toggle.
- Window centering.
- Mix of mouse and keyboard workflow.
- Focus with cursor.
- Normal Kill patch applied

<a href="https://user-images.githubusercontent.com/42818929/91505431-db19d900-e8cf-11ea-86bd-65f8b1096452.png"><img src="https://user-images.githubusercontent.com/42818929/91505431-db19d900-e8cf-11ea-86bd-65f8b1096452.png" width="43%" align="right"></a>

- Alt-Tab window focusing.
- No window borders.
- [No ICCCM](https://web.archive.org/web/20190617214524/https://raw.githubusercontent.com/kfish/xsel/1a1c5edf0dc129055f7764c666da2dd468df6016/rant.txt).
- No EWMH.
- etc etc etc

<br>

Patches available here: https://github.com/dylanaraps/sowm/pulls

## Default Keybindings

**Window Management**

| combo                      | action                 |
| -------------------------- | ---------------------- |
| `Mouse`                    | focus under cursor     |
| `MOD4` + `Left Mouse`      | move window            |
| `MOD4` + `Right Mouse`     | resize window          |
| `MOD4` + `f`               | maximize toggle        |
| `MOD4` + `c`               | center window          |
| `MOD4` + `Shift` + `q`     | kill window            |
| `MOD4` + `1-9`             | desktop swap           |
| `MOD4` + `Shift` +`1-9`    | send window to desktop |
| `MOD1` + `TAB` (_alt-tab_) | focus cycle            |
| `MOD4` + `F2`              | exit sowm              |

**Programs**

| combo                    | action           | program     |
| ------------------------ | ---------------- | ----------- |
| `MOD4` + `Return`        | terminal         | `st`        |
| `MOD4` + `d`             | dmenu            | `dmenu_run` |
| `MOD4` + `p`             | scrot            | `scr`       |
| `MOD4` + `w`             | wallpaper cycler | `bud`       |
| `XF86_AudioLowerVolume`  | volume down      | `amixer`    |
| `XF86_AudioRaiseVolume`  | volume up        | `amixer`    |
| `XF86_AudioMute`         | volume toggle    | `amixer`    |
| `XF86_MonBrightnessUp`   | brightness up    | `bri`       |
| `XF86_MonBrightnessDown` | brightness down  | `bri`       |

## Dependencies

- `xlib` (_usually `libX11`_).

## Installation

1. Copy `config.def.h` to `config.h` and modify it to suit your needs.
2. Run `make` to build `sowm`.
3. Copy it to your path or run `make install`.
   - `DESTDIR` and `PREFIX` are supported.
4. (Optional) Apply patch with `git apply patches/patch-name`
   - In case of applying multiple patches, it has to be done **manually**.

If you are using GDM, save the following to `/usr/share/xsessions/sowm.desktop`. It is still recommended to start `sowm` from `.xinitrc` or through
[your own xinit implementation](https://github.com/dylanaraps/bin/blob/dfd9a9ff4555efb1cc966f8473339f37d13698ba/x).

```
[Desktop Entry]
Name=sowm
Comment=This session runs sowm as desktop manager
Exec=sowm
Type=Application
```

## Thanks

- [2bwm](https://github.com/venam/2bwm)
- [SmallWM](https://github.com/adamnew123456/SmallWM)
- [berry](https://github.com/JLErvin/berry)
- [catwm](https://github.com/pyknite/catwm)
- [dminiwm](https://github.com/moetunes/dminiwm)
- [dwm](https://dwm.suckless.org)
- [monsterwm](https://github.com/c00kiemon5ter/monsterwm)
- [openbox](https://github.com/danakj/openbox)
- [possum-wm](https://github.com/duckinator/possum-wm)
- [swm](https://github.com/dcat/swm)
- [tinywm](http://incise.org/tinywm.html)

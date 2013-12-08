General Use
-----------

### Building

You can pass in the board type and layout while invoking the `make` command like
so: `make BOARD=phantom LAYOUT=ansi_iso`

Supported board/layout combos can be seen by running `make show_layouts`:

```
$ make show_layouts
BOARD=hid_liber LAYOUT=ansi_iso_jis
BOARD=phantom LAYOUT=ansi_iso
BOARD=phantom LAYOUT=ansi_iso_win
BOARD=pontus LAYOUT=pontus
BOARD=sskb LAYOUT=iso
BOARD=sskb LAYOUT=symmetric
BOARD=test32u2 LAYOUT=test
```

### Jump to HalfKay bootloader

This allows you to load new firmware without pressing the button on the Teensy.
With the teensy loader open, press `LSHIFT` + `RSHIFT` simultaneously. The
teensy should respond and jump into HalfKay.

### Making a custom keymap

Constants are defined in `usb_keyboard_debug.h` for most keypress actions you
will want to use. Find the key symbol you need, and then modify the profile file
([board]/[layout].c) you like to use it in place of some other key.

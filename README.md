# Custom Layout for QMK

This is my custom (kbd75 v2) keyboard's layout as defined in the QMK firmware.


## How to get it working

Follow the instructions [here](https://https://beta.docs.qmk.fm/tutorial/newbs)
to install QMK on Linux.

When you get to the "Open keymap.c In Your Favorite Text Editor" paragraph
in "Building Your First Firmware", substitute keymap.c with the file in this repo.

NOTE: qmk compile and qmk flash are a bit weird with the paths they want, e.g. in
```
qmk compile -kb kbdfans/kbd75/rev2 -km ISO-swapesc -j 8
```
Notice that the keyboard path is not the full path (which would be keyboards/kbdfans/blabla), and the keymap is just the name of it.

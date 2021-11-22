# Custom Layout for QMK

This is my custom (kbd75 v2) keyboard's layout as defined in the QMK firmware.


## How to get it working

Follow the instructions [here](https://https://beta.docs.qmk.fm/tutorial/newbs)
to install QMK on Linux.

When you get to the "Open keymap.c In Your Favorite Text Editor" paragraph
in "Building Your First Firmware", substitute keymap.c with the file in this
repo. Then, compile and flash the firmware as below:

```
qmk compile -kb kbdfans/kbd75/rev2 -km ISO-swapesc -j 8
qmk flash -kb kbdfans/kbd75/rev2 -km ISO-swapesc
```

NOTE: qmk compile and qmk flash are a bit weird with the paths they want,
e.g. in
```
qmk compile -kb kbdfans/kbd75/rev2 -km ISO-swapesc -j 8
```
notice that the keyboard path is NOT the full path like
```
keyboards/kbdfans/kbd75/rev2
```

and the keymap is just the name of the keymap, not the full path.


This repository also contains the config.h file. This is supposed to be
copypasted into the keyboard directory of QMK, e.g.
```
keyboards/kbdfans/kbd75/rev2/config.h
```
For reference, the only non-standard thing is a higher than default debouncing
delay (to avoid occasional double presses).

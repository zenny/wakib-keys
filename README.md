# wakib-mode
Emacs mode that moves to modern keybindings

This mode that in my humble opinion is needed to give Emacs some
modern shortcuts.


## Installation

Just copy the wakib-mode.el file to the location in your emacs loadpath
and put

```
(require 'wakib-mode)
(wakib-mode 1)
```
in your init.el file

## Features

Proper CUA editor

Moved the common Emacs prefixes to free up key for proper copy-cut shortcuts

The new prefixes are

C-c => C-d
C-x => C-e

This moves the prefixes to two keys that to my knowledge aren't commonly mapped
and can be reached very easily.

Please note that only the prefix key changes in emacs commands, so the vanilla
Emacs C-c C-c press becomes C-d C-c in this mode.

This minor mode is heavily influenced by Ergoemacs mode. So movement is by
using Alt + ijkl keys. I hope to finish up the keybindings soon. This is
modifier based mode. If you are looking for a modal keybinding in the same
vein, check out xah-fly-keys.

Much thanks to the general.el project for giving me the solution of
dynamically binding prefix keys. If you simply want to copy the C-c key
to another location, while keeping C-c as is, check them out, they provide a
an easy way of doing it. Or just check out the Macro shown in my mode.

## Warnings

The C-c key doesn't return to normal after you turn of wakib mode. You need
to run
```
(setq wakib-cc-mode nil)
```
to get it back. I will bind this the mode-hook on mode disable once I figure
it out.

It seems C-x is overwritten on certain occasions due to minor modes actually
using it (who knew). I will implement the same override for C-x as I did for
C-c to handle those.

I am very very new to elisp, and emacs so any suggestions or advice is
greatly appreciated.
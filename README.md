# QMK Userspace

All of my personal keyboard files and notes about [QMK](https://qmk.fm/) (Quantum Mechanical Keyboard) firmware.

## Structure

```
.
├── keyboards/					# Keyboard specific files
│   └── .../keymaps/<keymap>/	# Keymap specific files
│       ├── features/
│       │   └── ...				# Feature code
│       ├── keymap.c			# Keymap
│       └── rules.mk			# Keymap make rules
├── .clang-format
├── .clangd
├── .editorconfig
├── .gitignore
├── compile_commands.json		# See resources (4)
├── Makefile
└── qmk.json
```

\* Structure is subject to change as I become more acquainted with QMK firmware.

## Commands

-   `qmk new-keymap -kb <keyboard>` to create a new keymap.
-   `qmk compile -kb <keyboard> -km <keymap>` to compile a keymap.
-   `qmk flash -kb <keyboard> -km <keymap>` to flash your keyboard with new firmware.

## Resources

I highly recommend these resources if you're new to QMK or interested in mechanical keyboards.

1.  [QMK Guide](https://docs.qmk.fm/newbs) for the very basics.
2.  [QMK Keycodes](https://docs.qmk.fm/keycodes) for a list of all QMK keycodes.
3.  [Here](https://docs.qmk.fm/feature_layers#example-keycode-to-cycle-through-layers) for layer cycling.
4.  [Here](https://docs.qmk.fm/cli_commands#qmk-generate-compilation-database) for questions about `compile_commands.json` and fixing red squiggles.
5.  [SOCD Cleaner](https://getreuer.info/posts/keyboards/socd-cleaner) for implementing SOCD similiarly to Wooting keyboards.
6.  [Pascal Getreuer](https://getreuer.info/posts/keyboards) for other interesting feature implementations.
7.  [Monkeytype](https://monkeytype.com) for a customizable typing test.

## TODO

-   Abstract feature files.
-   Create reusable make rules.
-   Create reusable config file.
-   Document and reorganize kbd75 keymap.

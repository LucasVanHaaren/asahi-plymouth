# Asahi Linux Plymouth Theme

This is a Plymouth theme for the Asahi Linux distribution for Apple Silicon Macs.
It's probably janky as hell.


## Installing (for Arch-based distros)
You should have Plymouth installed and hooked into your initrd.

1. Clone this repo somewhere.
2. Copy the `asahi` folder to `/usr/share/plymouth/themes/`.
3. Run `plymouth-set-default-theme -R asahi` as root.
Note that this procedure works for Arch and its forks. Adding -R
rebuilds the initrd automatically. For other distros, you will have to
figure out how to set your Plymouth theme and update the initrd yourself.

## Testing
1. Run `plymouthd --no-daemon --debug` as root in tty2.
2. Run `plymouth show-splash` in tty3. The splash screen
will appear in tty1.
* Running `plymouth` with no arguments will give you a list of
modes and parameters you can test.

## What works
* The Asahi Linux logo shows up
* The beachball spins
* The progress bar fills up while booting
* Boot time messages appear below the progress bar

## Yet to be implemented
Password/text entry (required for users with LUKS-encrypted disks, etc.).
I had a go at this myself, but I could not get it to work at all. Every other
Plymouth theme just copies the reference script, however
* It's an uninteligible spaghettified mess
* I refuse to copy code that is not mine and I do not understand
Please feel free to fork this repo and come up with a solution yourself.

## Attributions
* The Asahi Linux logo was created by <a href="https://soundflora.tokyo/">soundflora*</a> and <a href="https://github.com/marcan/">Hector Martin</a>. It is available under the CC BY-SA 4.0 license.

* The Apple-like beachball is available for free for non-commercial use from
<a href="https://pngwing.com">PNGWing</a>.

---
layout: markdown
title: Changelog
---

#### [0.7.2] - 2018-12-16
- Makefile added
- Proper App Icons!!
- Better Table of Contents in `README.md`
- Added tutorial to `README.md`
- Tested GoboLinux compatibility (weird but cool distro)
- Desktop file works with Flatpak (not tested for native installations)
- AppStream Metadata conforms to Freedesktop and Flathub standards
- No longer using `/tmp` under Flatpak (using wrapper script)
- Bug fix where multiple "zombie" processes would stay alive (pun not intended) after sending a tweet/toot

#### [0.7.1] - 2018-12-07
- Fixed TMPDIR in Flatpak (fixed an issue where it wouldn't open the screenshot you took)

#### [0.7.0] - 2018-12-07
- Flatpak works on GNOME Wayland/X11 systems
- Flatpak integrates gnome-screenshot and feh
- Fixed glib/gio issue where multiple instances of ShareXin wouldn't launch, and only one would be allowed

#### [0.6.9] - 2018-12-07
- Removed Clipboard functionality (doesn't work under Wayland)
- Flatpak fixes

#### [0.6.8] - 2018-11-02
- Moved anything in `cmd.rs` to `main.rs` (main only called cmd anyways)
- Moved anything in `save.rs` to `image.rs`
- `error.rs` is now `text.rs`, also merged with `language.rs`
- Reorganized things to accommodate for Flatpaks
- Added Flatpak!!!
- Tried to simplify a LOT of code
- `error.rs` now contains some planned enums for future rewritten error handling
- Fixed bug where some errors were not found in YAML files for some reason
- Fixed bug where because the `ShareXin` folder in pictures was already created, it attempted to display an error, which crashed for some reason
-
- Slightly modified Headerbar
- "Sent to Twitter" and "Sent to Mastodon" notifications disappear from your Notifications and don't stick around in the OSD

#### [0.6.7] - 2018-10-21
- Colours for character count on message popup match colours on Twitter Web
- Character count on message popup turns yellow when approaching limit with 20 characters left, just like on Twitter Web
- Didn't know `unreachable!("")` was a thing, replaced some instances of `panic!()` with it
- Removed useless `error::fatal()` message
- Disabling *"Ok"* button when no text is entered or when too much text is over service limit
- Removed "File saved" notification, not really needed
- Updated dependencies
- Debian is actually compatible **(had to regress from 3_22_30 of gtk-rs to 3_18)**
- Better comments
- `--upgrade` removed due to issues with openssl
- Character count only changes when keys are pressed in the TEXT Box, not the entire window
- Made `error.rs` actually readable
- Notifications for a sent image or status tweet/toot or Imgur post only last 2 seconds

#### [0.6.6] - 2018-10-31
- More testing done
- Removed some strange and unnecessary lines
- Removed lots of duplicate code
- Replaced many if else statements with match statements
- AppImage script provided
- General bug fixes
- Split screenshotting functionality off to [screenshot-rs](https://github.com/ShareXin/screenshot-rs)
- Removed swaywm support (even back when I used it, my implementation was trash, if any this is a service to sway users)
- Removed RefCell in `dialog.rs`
- Updated Twitter character limit (not full proof for non-Latin characters)
- Heavy rewrite of functions with clearer variables
- Old Twitter API restored for functionality, will be replaced by native API in a later update

#### [0.6.5] - 2018-09-26
- Work will continue on the project!
- Updated GNOME deps to 3_22_30 from 3_10
- Removed macOS support (how many people even used it?)
- Removed tray icon support (unneeded and unusable, GNOME doesn't even support it anymore)
- Updated various dependencies
- Removed ShareXin as a library
- Readded ShareXin to crates.io
- Added Subfolder under ShareXin in Pictures for sorting by years-month
- Rewrote method of determining screenshot selection software
  - Used to rely on hard-coded desktop variables to match with specific software
  - Now simply checks which software is installed, in a preferred order
- `t` and `toot` are still required for use with Twitter and Mastodon, but this WILL be addressed in 0.6.6
  - Native rust Twitter and Mastodon APIs will be added, with hopefully the same functionality.
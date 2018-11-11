---
layout: markdown
title: Code contribution
---

## Requirements

* Linux or FreeBSD
* rustc 1.30.1^

## Code formatting

I use `cargo fmt` for automatic formatting of Rust code.

## Possible contributions

* Enhancements to Flatpak, AppImage, or AUR packaging files
* Submissions for translations
* UI enhancements
* Uploaders (you must modify `main.rs` to include your own source, and edit Cargo.toml to include your dependencies, and you must create arguments in `main.rs` CLI parser to use your uploader)
* Improvements to current Twitter/Mastodon uploaders (currently, they use `t` and `toot` CLI apps for actually sending Tweets/Toots. I plan on replacing these with native Rust APIs for Twitter and Mastodon.)
* Improvements to `screenshot-rs` (not in main repo but in ShareXin project, provides screenshotting functions to ShareXin)

<!--
SPDX-FileCopyrightText: 2020 George Florea Bănuș <georgefb899@gmail.com>

SPDX-License-Identifier: CC-BY-4.0
-->

### [Read before reporting a bug or requesting a feature](./bugs_and_feature_requests.md)

----

#### Donate: [GitHub Sponsors](https://github.com/sponsors/g-fb) | [Liberapay](https://liberapay.com/gfb/) | [PayPal](https://paypal.me/georgefloreabanus)

# Haruna Mix

Haruna Mix is a fork of Haruna that allows simultaneous audio track selection.
Check or uncheck individual tracks in **Audio → Track** to change the mix.
Selecting one track restores normal playback; unchecking every track disables audio.
The selection resets when opening another file.

Haruna is an open source media player built with Qt/QML and libmpv.

![Haruna main window](./data/screenshots/haruna-dark.png)
For more screnshots go to [Haruna's website](https://haruna.kde.org)

# Install

<a href='https://flathub.org/en/apps/org.kde.haruna'><img width='190px' alt='Download on Flathub' src='https://flathub.org/assets/badges/flathub-badge-en.png'/></a>

```
flatpak install flathub org.kde.haruna
flatpak run org.kde.haruna
```

[Flatpak setup guide](https://flatpak.org/setup/)

# Features

these are just some features that set Haruna apart from others players

- video preview on seek/progress bar

- play online videos, through youtube-dl

- toggle playlist with mouse-over, playlist overlays the video

- auto skip chapter containing certain words

- configurable shortcuts and mouse buttons

- quick jump to next chapter by middle click on progress bar

- custom mpv commands, can be run at start up or on keyboard shortcut

# Dependencies
Dependencies will be printed by `cmake` when building.

# Build

```bash
git clone https://github.com/daddyparodz/haruna-mix.git
cd haruna-mix
cmake -S . -B build -G Ninja -DCMAKE_BUILD_TYPE=RelWithDebInfo
cmake --build build --parallel
./build/bin/haruna
```

Build locally with a C++ compiler, CMake, Ninja, Qt 6.9 or newer, KDE Frameworks
6.24 or newer, MpvQt, KDSingleApplication, and the FFmpeg development libraries.
CMake reports any missing dependencies. No GitHub Actions are required.

To install the completed build, run `cmake --install build --prefix /your/prefix`.

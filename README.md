# FlipAmiibo

Fork of Firefox2100's AmiTool.

A Flipper Zero toolkit to work with Amiibos.

This project is usable but still in development. Ensure you back up all important data and avoid using it with another experimental setup to prevent damage or data loss.

## Features

- **Reading NTAG215 character NFC tags**: Read data from physical NTAG215 gaming tags and store it on the Flipper Zero.
- **Displaying character information**: Show detailed information about the tag, including character name, series, type, usage, and other metadata. This information is sourced from the AmiiboAPI (https://amiiboapi.org/).
- **Emulating NTAG215 gaming NFC tags**: Emulate the loaded data, allowing the Flipper Zero to function as the corresponding character tag.
- **Writing game data to NFC tags**: Write currently loaded tag data to blank NTAG 215 tags, or a compatible device.
- **Generating character data**: Create a synthetic character data structure based on selected character.  The result would be a blank data file that can be written to a blank NTAG 215 tag, with no owner or game information.
- **Randomising the unique identifier (UID)**: Modify the UID of the loaded character data to a random valid value, allowing one tag to be used as multiple different tags.
- **Emulating a blank tag**: Emulate a blank NTAG 215 tag that can be written into with other devices.
- **Saving and loading character data files**: Store generated or read data files on the Flipper Zero's storage for later use.

## Installation

- Download the latest release from the [Releases](https://github.com/AzaharPlus/FlipAmiibo/releases) page.
- Copy the `flip_amiibo.fap` file to the apps directory on your Flipper Zero's storage.
- Restart your Flipper Zero to load the new app.

## Usage

**Main Menu**

![Amiibo Toolkit Main Menu](docs/screenshots/main-menu.png)

**Read Amiibo Tag**

![Read Amiibo Tag](docs/screenshots/read-menu.png)

**Generate Amiibo Data**

![Generate Amiibo Data](docs/screenshots/generate-menu.png)

**Select Which Platform to Generate For**

![Select Platform](docs/screenshots/choose-platform.png)

**Select Game Series**

![Select Game Series](docs/screenshots/choose-game.png)

**Select Character**

![Select Character](docs/screenshots/choose-character.png)

**Amiibo Information Display**

![Amiibo Information Display](docs/screenshots/amiibo-info.png)

**More Amiibo Information Display**

![More Amiibo Information Display](docs/screenshots/amiibo-info-2.png)

**Emulate Amiibo Tag**

![Emulate Amiibo Tag](docs/screenshots/emulate-menu.png)

**Usage Info Display**

![Usage Info Display](docs/screenshots/usage-info.png)

**View Saved Amiibo Files**

![View Saved Amiibo Files](docs/screenshots/saved-menu.png)

## Acknowledgments

- Thanks to the Flipper Zero community and developers for their continuous support and inspiration.
- The data used in this project comes from AmiiboAPI (https://amiiboapi.org/).
- The algorighms and methods for character data manipulation are based on research and contributions from various online communities dedicated to Amiibo reverse engineering. Including but not limited to:
  * [Reverse Engineering Nintendo Amiibo (NFC Toy)](https://kevinbrewster.github.io/Amiibo-Reverse-Engineering/), containing a very detailed analysis of the data structure.
  * [amiitool](https://github.com/socram8888/amiitool), a command-line tool for manipulating dumped data. Note that the data is in a different format of what this project uses, and it won't work with the data stored with this app.
  * [weebo](https://github.com/bettse/weebo), another flipper zero NTAG215 tool, which uses amiitool, confirming (for me personally) that the flipper zero can handle the cryptography involved in data manipulation.

## Licenses

This project and its source code is licensed under the GNU General Public License v3.0 (GPL-3.0). See the [LICENSE](LICENSE) file for details. By using this project, you agree to comply with the terms of the GPL-3.0 license.

The data files used in this project are sourced from AmiiboAPI (https://amiiboapi.com/), which is licensed under the [MIT License](https://github.com/N3evin/AmiiboAPI/blob/master/LICENSE). A copy of it is included in the files directory for inclusion in the release package.

<h1 align="center">Ajour</h1>

![](./resources/screenshots/ajour-banner.png)

Ajour is a World of Warcraft addon manager written in Rust with a strong focus on performance and simplicity. The project is completely advertisement free, privacy respecting and open source. Ajour currently supports macOS and Windows.

<p align="center">
  <img width="600"
       alt="Ajour"
       src="./resources/screenshots/ajour-0.2.3.png">
</p>

![Quickstart](https://github.com/casperstorm/ajour/workflows/Quickstart/badge.svg)
![Security audit](https://github.com/casperstorm/ajour/workflows/Security%20audit/badge.svg)

## Features

- Addons from multiple repositories:
  - [wowinterface.com](https://www.wowinterface.com/addons.php)
  - [tukui.org](https://www.tukui.org/)
  - [curse](https://www.curseforge.com/wow/addons)
- Bulk update
- Remove addon
- Retail and classic flavor support
- Custom themes

## Install 

Prebuilt binaries for macOS and Windows can be downloaded from the [GitHub releases](https://github.com/casperstorm/ajour/releases) page.

For everyone else, a detailed instruction can be found [here](https://github.com/casperstorm/ajour/blob/master/INSTALL.md).

## Configuration

Ajour will generate a configuration file for you, unless it finds one in the following directory:

macOS / Linux:
- `$HOME/.config/ajour/ajour.yml`

Windows:

- `%APPDATA%\ajour\ajour.yml`

## Themes

Ajour supports Dark (default) and Light themes out of the box. Custom themes can also be added and selected inside the application.

Instructions for adding custom themes can be found on the [themes wiki page](https://github.com/casperstorm/ajour/wiki/Themes).

## FAQ

**_When will you release Ajour / be feature complete?_**

The plan is to have a stable, polished release in time for the Shadowlands launch. 10.27.20.

**_When can we expect a Linux version?_**

Ajour is being developed and tested on macOS and Windows, but should work on Linux if installed from source.

**_After updating an addon, it still says it can be updated. What gives?_**

Ajour does a "best effort" attempt at comparing the local addon version, with the latest version available online. Sometimes addon authors specify different versions when uploading their addon to a repository than what they have written in the addon itself. If the numbers don't match, Ajour will say an update is available every time the list is refreshed.

**_I'm using addon XYZ but I don't see it in Ajour. Why is that?_**

Ajour parses through the AddOns folder and uses a couple of rules to determine what to show (main addons) and not to show (dependencies). For example: If an addon does not specify a version in its .toc file, Ajour cannot determine if a newer version of it is available, and so we assume it's a dependency of another addon and hide it. 

If you are using an addon that Ajour doesn't list, we encourage you to raise an issue and tell us about it! We want Ajour to handle as many edge cases as possible. A collection of addons with known issues can be found in the [wiki](https://github.com/casperstorm/ajour/wiki/Addons-with-known-issues).

**_Why Rust?_**

We wanted to create an application which natively compiles to both Windows, Linux and macOS while at the same time is as performant and reliable as possible.

## Other addon managers

[Ogri'la](https://github.com/ogri-la) has done a great job of creating a curated list of other addon managers:

https://ogri-la.github.io/wow-addon-managers/

## Acknowledgement

- [tarkah](https://github.com/tarkah) for the many great contributions. 
- [Rasmus Nielsen](https://rasmusnielsen.dk/) for the Ajour icon.
- [mlablah](https://github.com/mlablah) for the architectural discussions.
- [##rust and the whole community 🦀](https://webchat.freenode.net/?channels=##rust)

## License

Ajour is released under the [MIT License.](https://github.com/casperstorm/ajour/blob/master/LICENSE)

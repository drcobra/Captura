# CapturaMOD

- Revereted back to 8 version because of GUI changes
- Can record in mono in MP3 & Vorbis
- Bigger visible list of devices

***
# Captura

[![Master Build Status](https://img.shields.io/appveyor/ci/MathewSachin/Captura/master.svg?style=flat-square)](https://ci.appveyor.com/project/MathewSachin/Captura)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE.md)
[![Chat](https://img.shields.io/badge/chat-on_gitter-yellow.svg?style=flat-square)](https://gitter.im/MathewSachin/Captura)
[![Downloads](https://img.shields.io/github/downloads/MathewSachin/Captura/total.svg?style=flat-square)](https://mathewsachin.github.io/Captura/download)
[![PayPal Donate](https://img.shields.io/badge/donate-PayPal-orange.svg?style=flat-square)](https://mathewsachin.github.io/Captura/donate)

&copy; [Copyright 2018](LICENSE.md) Mathew Sachin

:link: <https://mathewsachin.github.io/Captura/>

Capture Screen, WebCam, Audio, Cursor, Mouse Clicks and Keystrokes.

<a href="https://mathewsachin.github.io/Captura/screenshots"><img src="https://mathewsachin.github.io/Captura/assets/ScreenShots/Home.png" align="right"></a>

## Features

- Take ScreenShots
- Capture ScreenCasts (Avi/Gif/Mp4)
- Capture with/without Mouse Cursor
- Capture Specific Regions, Screens or Windows
- Capture Mouse Clicks or Keystrokes
- Mix Audio recorded from Microphone and Speaker Output
- Capture from WebCam.
- Can be used from [Command-line](https://mathewsachin.github.io/Captura/cmdline) (*BETA*).
- Available in [multiple languages](https://mathewsachin.github.io/Captura/translation)
- Configurable [Hotkeys](https://mathewsachin.github.io/Captura/hotkeys)

## Table of Contents

- [Installation](#installation)
  - [Setup](#setup)
  - [Portable](#portable)
  - [Chocolatey](#chocolatey)
  - [Dev Builds](#dev-builds)
- [Build Notes](#build-notes)
- [System Requirements](#system-requirements)
- [FFmpeg](#ffmpeg)
- Other Links
  - [Changelog](https://mathewsachin.github.io/Captura/changelog)
  - [Continuous Integration](https://mathewsachin.github.io/Captura/ci)
  - [Contributing](https://mathewsachin.github.io/Captura/contributing)
    - [Translation](https://mathewsachin.github.io/Captura/translation)
  - [Code of Conduct](https://mathewsachin.github.io/Captura/code_of_conduct)
  - [Command-line](https://mathewsachin.github.io/Captura/cmdline)
  - [FAQ](https://mathewsachin.github.io/Captura/faq)
  - [Hotkeys](https://mathewsachin.github.io/Captura/hotkeys)
  - [ScreenShots](https://mathewsachin.github.io/Captura/screenshots)
- [License](#license)

## Installation

There are a few different options for installing.

[latest]: https://github.com/MathewSachin/Captura/releases/latest

### Setup

Download and run `Captura-Setup.exe` for the latest release from [here][latest].

### Portable

Download and unzip `Captura-Portable.zip` for the latest release from [here][latest].

The settings are stored in `%APPDATA%/Captura` folder by default. You might want to customize this for the portable build using the `--settings` command-line argument.

### Chocolatey

```powershell
choco install captura -y
```

### Dev Builds

Dev builds can be unstable and should be used for testing purposes only.

1. Go to [AppVeyor project](https://ci.appveyor.com/project/MathewSachin/Captura) page.

2. Select Build Configuration: **Debug** or **Release**.

3. Open **Artifacts** tab.

4. Download **Zip package**.

## Build Notes

- [Visual Studio 2017](https://visualstudio.com) or greater is recommended.
- .Net Framework v4.6.1 is required.
- For detailed information, see [Building](https://mathewsachin.github.io/Captura/build).

## System Requirements

- Verified on **Windows 10**. Atleast Windows Vista is required.
- If you are on Windows 7 or earlier, make sure Aero is enabled.
- **Desktop Duplication API** is only available on **Windows 8** and above.
- 2 GHz CPU (Recommended).
- 4 GB RAM (Recommended).
- **.Net Framework v4.6.1** is required. You will be prompted to install if it is not already present on your system.
- Using the **FFmpeg Intel QSV HEVC** encoder requires the processor to be **Skylake (6th generation)** or later.
- For using `SharpAvi | Lagarith` codec, the Lagarith codec should be installed on your system and configured to use RGB mode with Null Frames disabled.

## FFmpeg

> It is recommended to always download the latest version of FFmpeg using FFmpeg Downloader. Older versions of FFmpeg can cause unexpected behaviour.

[FFmpeg](http://ffmpeg.org/) is an open-source cross-platform solution to record, convert and stream audio and video.
It adds support for more output formats like **H.264** for Video and **Mp3**, **AAC** etc. when capturing **Only Audio**.

FFmpeg is configured on the **FFmpeg** section in the **Configure** tab.

Due to its large size (approx. 30MB), it is not included in the downloads.
If you already have FFmpeg on your system, you can just set the path to the folder containing it.
If it is installed globally (available in PATH), you don't have to do anything.
If you don't have FFmpeg or want to update, use the inbuilt **FFmpeg Downloader**.
FFmpeg needs to be downloaded only once.

In cases where the **FFmpeg Downloader** fails, please download manually from <https://ffmpeg.zeranoe.com/builds/> and set FFmpeg folder in `Configure | FFmpeg`.

If you don't want to use FFmpeg, you can switch to `SharpAvi`.

## License

[MIT License](LICENSE.md)

Check [here](licenses/) for licenses of dependencies.

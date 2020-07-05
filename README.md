# KDiskMark
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-orange.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![GitHub (pre-)release](https://img.shields.io/github/release/JonMagon/KDiskMark/all.svg)](https://github.com/JonMagon/KDiskMark/releases)
[![Build Status](https://travis-ci.com/JonMagon/KDiskMark.svg?branch=master)](https://travis-ci.com/JonMagon/KDiskMark) 

KDiskMark is an HDD and SSD benchmark tool with a very friendly graphical user interface. KDiskMark with its presets and powerful GUI calls [Flexible I/O Tester](https://github.com/axboe/fio) and handles the output to provide an easy to view and interpret comprehensive benchmark result.

<p align="center">
   <img src="https://raw.githubusercontent.com/JonMagon/KDiskMark/master/assets/images/kdiskmark.png"/>
</p>

## Features
* Configurable block size, queues, and threads count for each test
* Many languages support
* Report generation

## Report Example
```
                             KDiskMark: https://github.com/JonMagon/KDiskMark
-----------------------------------------------------------------------------
* MB/s = 1,000,000 bytes/s [SATA/600 = 600,000,000 bytes/s]
* KB = 1000 bytes, KiB = 1024 bytes

[Read]
Sequential 1 MiB (Q= 8, T= 1):   531.561 MB/s [    531.6 IOPS] < 14416.00 us>
Sequential 1 MiB (Q= 1, T= 1):   451.977 MB/s [    452.0 IOPS] <  2199.04 us>
    Random 4 KiB (Q=32, T=16):    26.626 MB/s [   6816.4 IOPS] <  4684.30 us>
    Random 4 KiB (Q= 1, T= 1):    26.626 MB/s [   6816.4 IOPS] <  4684.30 us>

[Write]
Sequential 1 MiB (Q= 8, T= 1):   498.441 MB/s [    498.4 IOPS] < 15406.50 us>
Sequential 1 MiB (Q= 1, T= 1):   422.163 MB/s [    422.2 IOPS] <  2353.70 us>
    Random 4 KiB (Q=32, T=16):    19.768 MB/s [   5060.5 IOPS] <  6300.33 us>
    Random 4 KiB (Q= 1, T= 1):    19.768 MB/s [   5060.5 IOPS] <  6300.33 us>

Profile: Default
   Test: 32 MiB (x5) [Interval: 5 sec]
   Date: 2020/07/05 13:52:21
     OS: neon 18.04 [linux 5.3.0-62-generic]
```

## Dependencies
### Required
* GCC/Clang C++11 (or later)
* [CMake](https://cmake.org/) >= 3.5
* [Extra CMake Modules](https://github.com/KDE/extra-cmake-modules)
* Qt with Widgets >= 5.9
* [Flexible I/O Tester](https://github.com/axboe/fio) with libaio >= 3.1
    * If you build FIO from source, install `libaio-dev` package.

## Installation
Downloads are available on the [Releases](https://github.com/JonMagon/KDiskMark/releases/latest) page. 

## Localization
To help with localization you can use [Qt Linguist](https://doc.qt.io/Qt-5/linguist-translators.html). Add a new language file to the TS_FILES variable in CMakeLists.txt, translate it and create a pull request. 

Languages currently available:
* English (default)
* Russian
* German

## TODO
* Auto-detection disk manufacturer name
* Windows compatibility

## Credits
Application Icon  
Copyright (c) https://www.iconfinder.com/baitisstudio

If you have any ideas, critics, suggestions or whatever you want to call it, please open an issue.

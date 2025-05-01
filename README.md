# Random Number Generator Fix

[![Release](https://img.shields.io/github/v/release/StraDaMa/LC-Random-Number-Generator-Fix.svg)](https://github.com/StraDaMa/LC-Random-Number-Generator-Fix/releases)

<div align="center">
  <img src="https://i.imgur.com/Bschr4im.png" alt="MMBN1 unobtainable mystery data drop."/>
  <img src="https://i.imgur.com/hSr1wnUm.png" alt="MMBN4 unobtainable mystery data drop from this specific location."/>
  <img src="https://i.imgur.com/1k3i3GZm.png" alt="MMBN4 unencounterable random encounter."/>
</div>


This repo hosts the **Random Number Generator Fix** mod for **Mega Man Battle Network Legacy Collection Vol 1 and 2**, plus its issue tracker and releases.

## About
The Random Number Generator used in every Mega Man Battle Network game has a known bug, sometimes called the "RNG carryover glitch", that causes two subsequent calls to the RNG to sometimes lead to unintended odds for each possibility or some possibilities being omitted entirely. This most notably affects some Mystery Data drops and random encounters.

The shuffling algorithm used by the games is also known to not uniformly shuffle every item in the list, instead leaving items in their original positions more frequently.

This mod replaces the RNG and shuffling algorithms with ones that do not have these issues.

## Features
- Replaces the Random Number Generator with a xoshiro128** generator.
- Replaces the shuffling algorithm with an implementation of Fisher–Yates shuffle.
- Falls back to an implementation of the original RNG/shuffle  algorithms when in an online battle to prevent desyncs.
- Compatible with both **Vol. 1** and **Vol. 2** of the Legacy Collection.

## Installation

1. **Install chaudloader**  
   Download from the [chaudloader latest release](https://github.com/RockmanEXEZone/chaudloader/releases/latest).

1. **Locate game folder**  
   In Steam, right-click **Mega Man Battle Network Legacy Collection Vol. 1/2** → *Manage* → *Browse Local Files*.  
   If there’s no `mods` folder, create one.

1. **Copy the mod**  
   Download the latest [Random Number Generator Fix release](https://github.com/StraDaMa/LC-Random-Number-Generator-Fix/releases/latest), unzip, and place the `Random Number Generator Fix` folder into your `mods` directory.


    https://github.com/StraDaMa/LC-Random-Number-Generator-Fix/releases/latest

## Usage / Verification
1. Launch the game after installing chaudloader.
1. Check the box next to **Random Number Generator Fix**.
1. When the window opens, check the console you should see:
```txt
[mod: Random Number Generator Fix] Lua script complete
```
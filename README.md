# Hunter × Hunter: Maboroshi no Greed Island (English translation)

An English fan translation of **ハンター×ハンター 幻のグリードアイランド**
(*Hunter × Hunter: Maboroshi no Greed Island*), a PlayStation rougelike RPG
released only in Japan.

The patch translates the script, the menus, and every table the game reads
from: items, weapons, armour, Nen abilities, areas, shops, the quest log and
the ending score screen. It also replaces the fixed-pitch font with a
proportional one, so English text fits the game's windows instead of sprawling
out of them.

The staff credits are deliberately left in Japanese.

## What you need

This patch applies to **one specific disc image** and no other.

| | |
| --- | --- |
| Title | Hunter × Hunter: Maboroshi no Greed Island |
| Serial | **SLPM-86651** |
| Region | Japan (NTSC-J) |
| Publisher | Konami |
| Volume ID | `HUNTER_X_HUNTER` |
| Track | single track, `MODE2/2352` |

Your `.bin` must match these exactly:

| | |
| --- | --- |
| Size | `129,124,800` bytes |
| CRC32 | `AA4F8A5E` |
| MD5 | `e45f41d921a446d9eeed52c16bbe94e4` |
| SHA-1 | `af7f343cb4b2f3f5055cef78a5238d490c63c7da` |

There are two other versions of this game that have not been tested:
PSOne Books: SLPM-87205
Konami The Best: SLPM-86829
If you have either of these versions and want to help test, please contact me.

This is the Redump-verified dump of the retail disc. If your file is a
different size, is split into multiple tracks, or is a `.iso`, `.img`, `.pbp`,
`.chd` or `.ecm`, the patch will refuse to apply. Convert it to a single
`.bin` + `.cue` first.

**Do not ask where to get the disc image, and do not open an issue about it.**
See [Legal](#legal).

## Applying the patch

The patch is an **xdelta3** file, `hxhgi-vwf.xdelta`. It never modifies your
original; it writes a new, patched image alongside it.

### Windows, the easy way

1. Download [Delta Patcher](https://github.com/marcrobledo/delta-patcher/releases).
2. Open it, set **Original file** to your `.bin`, set **XDelta patch** to
   `hxhgi-vwf.xdelta`.
3. Press **Apply patch**.

### Any platform, on the command line

```sh
xdelta3 -d -s "Hunter x Hunter - Maboroshi no Greed Island (Japan).bin" \
        hxhgi-vwf.xdelta \
        hxhgi-en.bin
```

`xdelta3` is in most package managers (`apt install xdelta3`,
`brew install xdelta`, `pacman -S xdelta3`).

### Make the .cue

The patch produces a `.bin` only. Put a text file named `hxhgi-en.cue` beside
it containing:

```
FILE "hxhgi-en.bin" BINARY
  TRACK 01 MODE2/2352
    INDEX 01 00:00:00
```

The name inside the `.cue` must match your `.bin` exactly. Load the **`.cue`**
in your emulator, not the `.bin`.

## Verifying the result

The patched image should be:

| | |
| --- | --- |
| Size | `129,124,800` bytes |
| CRC32 | `7D778335` |
| MD5 | `1e2abc4971f5f52620838454ed6ebe65` |
| SHA-1 | `0db02103ae4368e0d4a1d26ce3d4fa1fcea0d61a` |

If these do not match, your source image was not the one described above.

## Playing it

Tested on **DuckStation**. Any accurate PlayStation emulator should work, and
so should real hardware via an optical drive emulator.

Save files from an unpatched copy are compatible, because the patch changes no
save data.

## Legal

**You must supply your own copy of the game.**

What is distributed here is **no copyrighted material from the game**, only a
*patch*: a file describing the differences between your disc image and a
translated one. It is useless without a legitimate copy of the original.

- No disc image, ROM, executable or asset from the game is distributed here,
  and none will be. Requests for one will be closed.
- *Hunter × Hunter* is the property of Yoshihiro Togashi, Shueisha and its
  licensors. The game is the property of Konami. This project is not
  affiliated with, endorsed by, or connected to any of them.
- This is an unpaid fan work, made for preservation and study, and distributed
  free of charge. It is not for sale, and neither is anything made from it.
  **Do not sell this patch, or any disc, cartridge, console or download
  containing it.**
- Dumping a disc you own for your own use is legal in some countries and not
  in others. Check your own jurisdiction.

If you represent a rights holder and want this taken down, open an issue and
it will be.

## Thanks

To the [RIBAIAN walkthrough](https://gaming.main.jp/hxhmaborosi/).

To [Hunterpedia](https://hunterxhunter.fandom.com/).

To the Redump project, for the disc verification this patch depends on.

## Game information and guides

<https://www.zerohash.net/hunter-x-hunter-maboroshi-no-greed-island/>


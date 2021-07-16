# uya-patch

Patches applied to all Ratchet & Clank Up Your Arsenal PS2 clients connecting to [Clank](https://github.com/hashsploit/clank).

Based on [deadlocked-patch](https://github.com/Dnawrkshp/deadlocked-patch) by [Dnawrkshp](https://github.com/Dnawrkshp).

## Build

You'll need a local copy of the [PS2SDK](https://github.com/ps2dev/ps2sdk). I recommend using docker. Instructions for how to build using docker are below.

If you are using a local copy, make sure you install [libuya](https://github.com/hashsploit/libuya) first.

Clone the repo and enter it:
```sh
git clone https://github.com/hashsploit/uya-patch.git
cd uya-patch
```

If you want to use docker, run the following commands:
```sh
docker pull ps2dev/ps2dev
docker run -it --rm -v "$PWD\:/src" ps2dev/ps2dev
cd src
./docker-init.sh
```

Then you can build using:
```sh
make
```

## Memory Usage

```arm
0x000C8000 - 0x000CF000 ; Gamerules
0x000CF000 - 0x000D0000 ; Module Definitions
0x000D0000 - 0x000D8000 ; Patch
0x000D8000 - 0x000DC000 ; Gamemode
0x000E0000 - 0x000F0000 ; Map loader irx modules
```

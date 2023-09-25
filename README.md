# Digimon World 2003 NTSC
Patch that makes Digimon World 2003 run as NTSC

## Why?
Digimon World 3 has 3 versions
- Digimon World 3 US (NTSC)
- Digimon World 3 JP (NTSC)
- Digimon World 2003 (PAL)

Out of the 3 versions only JP and 2003 have the post game, and only US and JP run in 60 fps (NTSC). This patch makes 2003 run in 60 fps on an NTSC console.

## Running
Some emulators will not run this correctly
- RetroArch
	- Beetle HW - won't run properly (sound desync)
	- ReArmed - will run properly, you have to force region to NTSC
	- SwanStation - runs properly out of the box
- PCSX-Redux - runs properly out of the box
- Duckstation - runs properly out of the box
- Real Hardware - untested, should in theory run fine on an NTSC console

## Patching
Download either the IPS or XDELTA patch
Patch **your** copy of Digimon World 2003 with
[IPS Patcher](https://www.romhacking.net/patch/)
[XDELTA Patcher](https://www.romhacking.net/utilities/598/)

## How it works
Fortunatly the devs left us 2 flags that are required for this to work
- 0x8005CCAC controls video mode and timings (0 PAL, 1 NTSC)
- 0x8005CCB0 controls frame buffer offset (1, no offset, 0 24 px offset)
By toggling these two flags we achieve seamless 2003 in NTSC
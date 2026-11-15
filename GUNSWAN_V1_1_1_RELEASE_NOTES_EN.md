# GunSwan v1.1.1 (Windows x64)

Fixed in-game save failures for some WonderSwan cartridges whose ROM footer declares a smaller SRAM size than the cartridge uses. GunSwan now treats the standard cartridge 8 KiB SRAM declaration (`0x01`) as 32 KiB in the shared cartridge code. No ROM modification is needed. Loading a recovered 32 KiB save via Continue was verified on the unmodified STAR HEARTS ROM.

On Windows, GunSwan preserves the original 8 KiB data at the start of the expanded save and backs up the original `.sav` as `.sav.8k.bak` before writing the first 32 KiB save. Existing corruption is not repaired automatically. States and Sessions recorded with the old 8 KiB layout may be rejected when their SRAM layout differs.

The included GunPuzzle for WSC - GunSwan Demo - is identical to the sample in v1.1.0. See known_limitations_ja.md in the package for continuing limitations.

[Download](https://github.com/yosisato-boop/GunSwan-Releases/releases/tag/v1.1.1) / [License (Japanese)](GUNSWAN_V1_1_1_BINARY_LICENSE_JA.md) / [Build provenance](GUNSWAN_V1_1_1_BUILD_PROVENANCE.json)

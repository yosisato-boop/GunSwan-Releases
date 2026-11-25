# GunSwan 1.2.0 — Windows x64

## Changes since v1.1.1

- REP transfers resumed by IRET can accept a subsequent interrupt during the transfer. This corrects the interrupt path associated with dialogue-window flicker and interrupted battle music in Final Fantasy.
- AAM and AAD use the instruction immediate. In line with hardware observations, DIV, IDIV and AAM 00 save the next instruction IP on INT0.
- D6 now sets AL to FFh and preserves AH and FLAGS, as observed on WonderSwan Color hardware. PUSHF, interrupts and exceptions now save the observed fixed and reserved PSW bits.
- Corrected timer I/O, interrupt base (INT_BASE) and palette I/O behavior.
- Eligible older states can be used to continue play. Migration retains the original state, and new saves use the current model's slots. Persistent SRAM, EEPROM and RTC data formats are unchanged.
- Regression testing covered reaching gameplay and basic input in all 55 Owned55 titles over their defined test segments.

## Upgrading from Windows v1.1.1

Choose **Start from State** in the Launcher, or use `--load-state` when starting GunSwan. A successful migration opens a new Session and retains the original state file. States whose interrupt state cannot be reconstructed safely are rejected; open those in the version that created them. In-game Quick Load uses the current model's save slots.

| Recording or state | Compatibility |
|---|---|
| Eligible older save state | Continue in a new Session |
| Supported older Session v3 | Best Effort playback; video, audio, and progress can differ |
| Older r1 GSXSESS or strict playback of an older recording | Use the build that recorded it |
| New v1.2.0 recording | Strict verification under compatible v1.2.0 execution conditions |

A **ROM-adjacent `.sav`** carries over on a normal launch when automatic cartridge saves are enabled and the file size matches the cartridge's save device. **Start from State** and **Continue Session** in the Launcher restore the cartridge save from the State. On normal exit, GunSwan overwrites the ROM-adjacent `.sav` with the current cartridge save. Resuming an older State can roll back your in-game save. States and Sessions with the former 8 KiB SRAM layout cannot be opened under the current 32 KiB layout. Eligible 8 KiB raw `.sav` files can still be imported.

An eligible State for the same ROM resumes on the model it was saved with. Switching between WS, WSC, and SwanCrystal does not resolve a CPU timing or save capacity mismatch. See `known_limitations_ja.md` in the distribution ZIP for the affected titles and details.

## Package

Extract the distribution ZIP to a new folder and start `gunswan-launcher.exe`. Use the accompanying checksum to verify the ZIP, and `SHA256SUMS.txt` to verify the extracted files. See `LICENSE.txt` for the license and `release-manifest.json` for build provenance.

[Download](https://github.com/yosisato-boop/GunSwan-Releases/releases/tag/v1.2.0) / [License (Japanese)](GUNSWAN_V1_2_0_BINARY_LICENSE_JA.md) / [Build provenance](GUNSWAN_V1_2_0_BUILD_PROVENANCE.json)

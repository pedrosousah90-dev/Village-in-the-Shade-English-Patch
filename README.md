# Village in the Shade — English Translation

Unofficial English translation patch for **Steam build 25311513 (v1.10)**.

This project ports the community English translation from Steam build **25094764 (v1.09)** to the current v1.10 build, rebuilt against that build's clean archives so the update's new content (including the new Simplified Chinese language slot, the extra font profile and the updated credits artwork) stays intact.

Current package: `build25311513-translation-port-20260915-v9`

> **Status:** playable start to finish. The text is complete and checked for rendering, and the sentences that the v1.09 translation cut off at the end of a page have been completed. The only known display issue is the name entry screen — see [Known Issues](#known-issues).

## Download

**[Download the latest release](../../releases/latest)**

### Requirements

- Windows
- A legitimate copy of *Village in the Shade* on Steam
- Steam build **25311513 (v1.10)**
- Approximately **7 GB of free space** on the game drive during installation

## Installation

1. Close the game.
2. Extract the package into the *Village in the Shade* game folder.
3. Run `Install English Translation Only.cmd`.
4. Start the game.
5. Select the **Japanese display-language slot** to use English.

The package includes tools to verify and restore the original game files.

## Installation & Test Video

[https://youtu.be/odNLgg76V1A](https://www.youtube.com/watch?v=odNLgg76V1A)

## What's Included

- English dialogue, database text, menus, NPC names and UI labels — 54,711 translated strings across 33 database tables.
- Lora font in the Japanese-slot profile of all five fonts, with the dialogue font sized for the English text.
- The official English minimap, button-icon and lost-book textures selected in the Japanese texture slot.
- 76 translated Fairy UI/art resources, rebased onto the current archive. The localization credits image was redrawn by v1.10, so it keeps the new v1.10 artwork and only takes the translated "Localization" header.
- Current v1.10 content, nonlocalized databases, scripts and unrelated artwork left untouched.

Only `data.dat` and `data\fairy_1_00.dat` are patched. The official `data\texture_1_00.dat` remains unchanged.

## Fixes over the original v1.09 translation

- **About 1,180 cut-off sentences completed.** The v1.09 English cut sentences at the end of a dialogue page (for example "...and you'll collapse on"). The endings do not exist anywhere in the old files, so they were rewritten from the Japanese — main story, tutorial, events, quests, holidays and villager daily chatter.
- The second half of the cemetery (gravetending) event was retranslated; its v1.09 English was corrupted into fragments.
- Villager requests name the item again. The v1.09 text dropped the item placeholder from all 14 villagers' request lines, so they only asked for "something I need".
- Restored missing quest details: the beehive errand asks for 5 bees again, and the hokora errand asks you to report back.
- Tips and item descriptions were re-wrapped to fit their boxes instead of overflowing, and the clinic sign's cut-off note was restored.
- Menu and settings labels that appeared as empty boxes (leftover Japanese and full-width characters that the English font cannot draw) were replaced.
- Unbalanced text markup and lost placeholders were checked table by table against the Japanese.

## Known Issues

- **Name entry screen** (your character, your dog, etc.): the keyboard opens in a Japanese kana mode whose letters cannot be drawn with the English font, so the grid looks empty. Click **Aa** at the bottom to switch to the alphabet keyboard before typing. The Hiragana and Katakana modes do not work with this patch. The "x" marks under the name are normal empty-slot markers; if boxes end up in the name, remove them with Backspace.
- Some lines were rewritten or shortened to fit the space available on screen, so they may differ from the original v1.09 wording.
- Minor text issues may still remain. Reports are welcome — see [Reporting issues](#reporting-issues).

## Verify / Restore

The package includes:

- `Verify Translation.cmd` — checks whether the installed files are clean, correctly translated, or modified/damaged. It also prints the installed package version, which is useful when reporting a problem.
- `Restore Original Translation.cmd` — restores the original v1.10 files captured during installation.

Close the game before installing, verifying or restoring the translation.

## Reporting issues

Please open an issue with:

1. The package version printed by `Verify Translation.cmd`.
2. A screenshot, or the text of the line and where it appears (character, place, time of day, event or quest).

## Screenshots

### Dialogue

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b6135ec5-0cc7-4e38-9226-40c11bfe65f3" />


### UI

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/1e6a308e-a4a6-4a84-8758-3a95e431331c" />


### Name Selection

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/22d9d113-9e6f-443a-acc5-725817a84931" />

### Title Screen

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/0885a599-4887-421d-b4e0-ee5eb73e8b99" />

### Save Data Screen

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/2505cc5f-714a-463e-88af-e143e36c4c43" />

## Safety & Integrity

- This package is **translation-only**. It does not modify the game's executable or DLLs, and it adds no gameplay features, input hooks or save modifications.
- It contains **reversible binary differences**, not game archives. No game file is redistributed here, and both patched archives keep their original size.
- Your save files are not touched. A backup before testing is still a good idea.
- The installer is a small unsigned Rust program, so antivirus software may flag it as an unknown publisher. Its full source and dependency lockfile are included in `source\patcher`, it makes no network connections, and it only reads and writes inside the game folder.
- `VillageInTheShadePatcher.exe` SHA-256: `db4dfce403a44167532ffc38cd7823fb880f807ff49412e920d3844a574db5d2`
- The SHA-256 of each release archive is published in its release notes.
- The tools used to port the translation are included in `source\port-tools`.

## Important

- Do not use the previous v1.09 translation files with v1.10.
- Steam updates may overwrite the translation. If that happens, the patch has to be rebuilt for the new build — restore the original files first and wait for an updated release.
- If the game fails to start, run `Restore Original Translation.cmd` before verifying the game files through Steam.

## Credits & Attribution

The original English translation/mod was obtained from the community release shared by **Switch On The Deck**.

**Original source:**

https://www.youtube.com/watch?v=l8VMQp8un0M

This project is an adaptation of the existing community English translation for Steam build **25311513 (v1.10)**.

This project does **not** claim authorship of the original English translation.

## Disclaimer

This is an unofficial fan-made project and is not affiliated with, endorsed by, or connected to the game's developer or publisher.

The game itself is not included with this project.

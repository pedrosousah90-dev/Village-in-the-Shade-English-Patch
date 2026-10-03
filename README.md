# Village in the Shade — English Translation

Unofficial English translation patch for **Steam build 25311578 (v1.20)**.

This project ports the community English translation from Steam build **25094764 (v1.09)** to the current game, rebuilt against each build's clean archives so the game's own updates stay intact. The current release covers **v1.20**, including everything that update added: new furniture, new livestock, the farmland expansion, the furniture catalog and the update notes screen.

Current release: **v1 for game v1.20** (`build25311578-translation-port-20261003-game1.20-v1`)

> **Status:** playable start to finish. The text is complete and checked for rendering, and the sentences that the v1.09 translation cut off at the end of a page have been completed. The only known display issue is the name entry screen — see [Known Issues](#known-issues).

> [!IMPORTANT]
> Releases **v1, v2, v2.1 and v2.2** were made for game **v1.10** and do **not** work on v1.20. If Steam has updated your game, use the latest release.

## Download

**[Download the latest release](../../releases/latest)**

### Requirements

- Windows
- A legitimate copy of *Village in the Shade* on Steam
- Steam build **25311578 (v1.20)**
- Approximately **9 GB of free space** on the game drive during installation

## Installation

1. Close the game.
2. Extract the package into the *Village in the Shade* game folder.
3. Run `Install English Translation Only.cmd`.
4. Start the game.
5. Select the **Japanese display-language slot** to use English.

The package includes tools to verify and restore the original game files.

**Coming from a release for v1.10?** Steam already replaced the translated files when it updated the game. Extract the new package over the old one and run `Install English Translation Only.cmd`. Don't run the old package's `Restore Original Translation.cmd` on v1.20. If the installer complains about unknown or mixed files, use Steam's **Verify integrity of game files** and install again.

## Installation & Test Video

[https://youtu.be/odNLgg76V1A](https://www.youtube.com/watch?v=odNLgg76V1A)

## What's Included

- English dialogue, database text, menus, NPC names and UI labels — 55,520 translated strings across 38 database tables, including all the text added by v1.20.
- Lora font in the Japanese-slot profile of all five fonts, with the dialogue font sized for the English text.
- The official English minimap, button-icon and lost-book textures selected in the Japanese texture slot.
- Translated UI and artwork (Item Request Form, calendar, date display, category tags, badges, livestock posters and more), including the four livestock posters added by v1.20.
- Current game content, nonlocalized databases, scripts and unrelated artwork left untouched.

`data.dat`, `data\fairy_1_00.dat` and `data\texture_1_00.dat` (summer and winter maps only) are patched.

## Fixes over the original v1.09 translation

- **About 1,700 cut-off sentences completed.** The v1.09 English cut sentences at the end of a dialogue page (for example "...and you'll collapse on"). The endings do not exist anywhere in the old files, so they were rewritten from the Japanese — main story, tutorial, events, quests, holidays and villager daily chatter.
- The second half of the cemetery (gravetending) event was retranslated; its v1.09 English was corrupted into fragments.
- Villager requests name the item again. The v1.09 text dropped the item placeholder from all 14 villagers' request lines, so they only asked for "something I need".
- Restored missing quest details: the beehive errand asks for 5 bees again, and the hokora errand asks you to report back.
- Letters, tips, item descriptions, reply choices, quest banners and other on-screen text were re-wrapped or shortened to fit their boxes, and artwork that did not match the current layout was redrawn.
- Menu and settings labels that appeared as empty boxes (leftover Japanese and full-width characters that the English font cannot draw) were replaced.
- A speech bubble that showed up completely empty, and lines that showed up twice, were fixed.
- Unbalanced text markup and lost placeholders were checked table by table against the Japanese.
- Spelling slips and duplicated words left in the v1.09 text were corrected ("wierdly", "I cant blame", "a way to to escape", and so on).

## Known Issues

- **Name entry screen** (your character, your dog, etc.): the keyboard opens in a Japanese kana mode whose letters cannot be drawn with the English font, so the grid looks empty. Click **Aa** at the bottom to switch to the alphabet keyboard before typing. The Hiragana and Katakana modes do not work with this patch. The "x" marks under the name are normal empty-slot markers; if boxes end up in the name, remove them with Backspace.
- Some lines were rewritten or shortened to fit the space available on screen, so they may differ from the original v1.09 wording.
- Minor text issues may still remain. Reports are welcome — see [Reporting issues](#reporting-issues).

## Verify / Restore

The package includes:

- `Verify Translation.cmd` — checks whether the installed files are clean, correctly translated, or modified/damaged. It also prints the installed package version, which is useful when reporting a problem.
- `Restore Original Translation.cmd` — restores the original v1.20 files captured during installation.

Close the game before installing, verifying or restoring the translation.

## Reporting issues

Please open an issue with:

- A screenshot, or the text of the line and where it appears (character, place, time of day, event or quest).
- The version (shown by `Verify Translation.cmd`).

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
- It contains **reversible binary differences**, not game archives. No game file is redistributed here, and every patched archive keeps its original size.
- Your save files are not touched. A backup before testing is still a good idea.
- The installer is a small unsigned Rust program, so antivirus software may flag it as an unknown publisher. Its full source and dependency lockfile are included in `source\patcher`, it makes no network connections, and it only reads and writes inside the game folder.
- `VillageInTheShadePatcher.exe` SHA-256: `39df1971370bb86f89a468149b10b45eafda7c38184529bf8fdc84f43cab7954`
- The SHA-256 of each release archive is published in its release notes.
- The tools used to port the translation are included in `source\port-tools` (the v1.10 → v1.20 port is in `source\port-tools\port120`).

## Important

- Do not use translation files made for an older game build with v1.20.
- Steam updates may overwrite the translation. If that happens, the patch has to be rebuilt for the new build — use Steam's **Verify integrity of game files** and wait for an updated release.
- If the game fails to start, run `Restore Original Translation.cmd` before verifying the game files through Steam.

## Credits & Attribution

The original English translation/mod was obtained from the community release shared by **Switch On The Deck**.

**Original source:**

https://www.youtube.com/watch?v=l8VMQp8un0M

This project is an adaptation of the existing community English translation for the current Steam builds of the game.

This project does **not** claim authorship of the original English translation.

## Disclaimer

This is an unofficial fan-made project and is not affiliated with, endorsed by, or connected to the game's developer or publisher.

The game itself is not included with this project.

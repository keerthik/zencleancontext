# Customized Zen Context Menu mod

[Original repository source](https://github.com/KiKaraage/ZenMods/tree/a6552b9ab17829d052832cdc091e3b19fa716616/Zen-context-menu)
[Original mod source](https://github.com/zen-browser/theme-store/tree/65a35f2fe25ce175f8fab0d21934f52916419a97/themes/81fcd6b3-f014-4796-988f-6c3cb3874db8)

This version makes a few opinionated cleanups. Here's what it looks like when I use it 
(I care about spaces and profiles, but not really most other tab context menu options):   

![simplified tab context menu](image.png)   

As of this commit, this theme isn't on the theme store.

Zen's "Import mods" button only re-downloads mods from the theme store, so it will not pick this up.

## Manual installation

`<profile-path>` below means your Zen profile folder:
- Windows: `C:/Users/<user-folder>/AppData/Roaming/zen/Profiles/<profile-folder>/`
- macOS: `~/Library/Application Support/zen/Profiles/<profile-folder>/`
- Linux: `~/.zen/<profile-folder>/`

1. Check out this repo or extract the downloadable zip archive.
2. Quit Zen.
3. Put the folder, or a symlink/junction to it, at `<profile-path>/chrome/zen-themes/korc_custom/`.
   The folder name must match the `id` in [example-zen-themes.json](example-zen-themes.json).
    - Windows (PowerShell, no admin needed):
      ```powershell
      New-Item -ItemType Directory -Force "$env:APPDATA\zen\Profiles\<profile-folder>\chrome\zen-themes" | Out-Null; New-Item -ItemType Junction -Path "$env:APPDATA\zen\Profiles\<profile-folder>\chrome\zen-themes\korc_custom" -Target "<path-to-this-repo>"
      ```
    - macOS / Linux:
      ```sh
      mkdir -p "<profile-path>/chrome/zen-themes" && ln -s "<path-to-this-repo>" "<profile-path>/chrome/zen-themes/korc_custom"
      ```
4. Register the mod in `<profile-path>/zen-themes.json` (next to the `chrome` folder, not inside it).
   If that file only contains `{}`, replace its contents with [example-zen-themes.json](example-zen-themes.json).
   Otherwise merge the `korc_custom` entry into the existing object.
5. Start Zen, open Settings > Mods, and flip any one of this mod's toggles off and back on.
   This makes Zen rebuild its mod stylesheet, and the menu changes apply.

## How Zen loads it

Below is tested with Zen 1.22.x.

Zen does not `@import` mod files. Whenever a mod is toggled, and on the first launch after a Zen update,
it regenerates `<profile-path>/chrome/zen-themes.css` from `zen-themes.json` by pasting each registered
mod's `chrome.css` into it. Hand edits to `zen-themes.css` are lost on every update, which is why the
mod has to be registered in `zen-themes.json` instead.

- After editing `chrome.css`, flip a toggle in Settings > Mods again to re-paste it. Restarting is not enough.
- If you installed via symlink/junction, do not use the "Remove" button in Settings > Mods. It deletes
  the mod folder from disk recursively (not just the symlink). 
   - Disable the mod with its toggle, or delete the link manually via Explorer/Finder/file browser.
# World of Darkness Statblock Template Guide
**Download & automatic installer instructions at the bottom!**

## The Template
- This template is designed for Atlas' native statblocks, which are currently an experimental feature. To enable it, open a scene, click the command button (`⌘`) in the toolbar, and search for "Experimental Features," then enable "Statblock editor."
- You can install the template and snippets automatically via the **Statblock Template Installer for Atlas** plugin (see [Automatic Installation](#automatic-installation-recommended) below), or manually place the `.atlastemplate` file inside a `statblock-templates` folder in your Obsidian vault. You can create statblocks based on the template by right-clicking any folder, choosing "New statblock here," and choosing this template.
- It is designed as a universal sheet for **World of Darkness 5th Edition** (supporting **Vampire**, **Werewolf**, **Hunter**, **Dhampir**, **Mage**, **Wraith**, **Changeling**, **Demon**, and **Mummy**).
- It is included in this repository as `World-of-Darkness-Character-Sheet.atlastemplate`.

### Points of Confusion
- **Dynamic Game Line (Splat) Switching:** Picking a game line from the **Game Line** dropdown (`Vampire`, `Werewolf`, `Hunter`, `Dhampir`, `Mage`, `Wraith`, `Changeling`, `Demon`, or `Mummy`) automatically reveals the lineage/identity fields, trackers (such as Hunger/Humanity, Rage/Renown, or Desperation/Danger), and power sections for that splat while hiding all others.
- **3×3 Arena × Approach Attribute Table:** Attributes are organized into a 3×3 grid with **Arenas** (`Physical`, `Social`, `Mental`) as rows and **Approaches** (`Force`, `Finesse`, `Resilience`) as columns:
  > **Physical:** Strength (Force), Dexterity (Finesse), Stamina (Resilience)
  >
  > **Social:** Charisma (Force), Manipulation (Finesse), Composure (Resilience)
  >
  > **Mental:** Intelligence (Force), Wits (Finesse), Resolve (Resilience)
- **Automatic Health & Willpower Calculation:** Base **Health** automatically calculates as `Stamina + 3` and **Willpower** calculates as `Composure + Resolve` unless overridden manually. (If you play a ruleset with a fixed track length, you can enter a manual number directly into the `Health` or `Willpower` field.)
- **How `used` Works on Dot & Box Trackers:** In Atlas' underlying YAML frontmatter, counter trackers store spent/empty pips as `used` (`filled pips = max - used`). On `Health` and `Willpower` boxes, `used: 0` means full health/willpower; on `1–5` dot ratings (like Skills or Disciplines), `used: 2` on a `max: 5` row displays 3 filled dots (`●●●○○`).
- **Dice Pool Formulas (`Nd10cs>=6`):** World of Darkness uses d10 dice pools rather than d20s. Power and weapon entries use Atlas' success-counting syntax (`6d10cs>=6`), which counts every die rolling `6` or higher as a success. Note that Atlas counts 1 success per `10` rather than WoD5's "pair of 10s = 4 successes" critical rule, so add `+2` successes mentally whenever you roll two or more `10`s.

## Known Issues
- I have not tested the template with the closed beta feature of Atlas called Atlas Online, or the unofficial community plugin Connect for Atlas. It will probably display badly in both of those, but I do not plan to investigate the issue until the official Online feature is in a full release for stability reasons.
- Clicking a cell in the 3×3 Attribute table rolls `{value}d10` (summing the dice) rather than `cs>=6`, because Atlas' built-in `scores` table block does not yet support custom roll suffixes.
- Atlas currently does not support automatically combining an Attribute dot rating and a Skill dot rating into a single pool button, so combined pools (such as `Dexterity + Stealth`) are entered directly on power/weapon entries or rolled from the dice tray.

## Additional Features
### Functional Layout Snippets
- **WoD5 Sheet Polish (`wod-sheet-polish.css`):** Strongly recommended. This snippet renders the 3×3 Attribute table with row labels (`Physical`, `Social`, `Mental`), individual attribute names, and clickable 5-dot pip bars; arranges Skills, Advantages, and Trackers into clean grids; prevents fraction counters from wrapping; and styles powers and weapons as compact cards.
- **Two-Column Hover Preview (`two-column-hover.css`):** Optional snippet to force statblock previews (when hovering over a token in a scene) to render in two columns for readability.

### Themes
- All visual themes from the 5e repository are included here as optional Obsidian CSS snippets. They do not affect functionality. I personally recommend **`gothic.theme.css`** for WoD, though any theme should work.
- If you use the automatic installer plugin, all themes are downloaded into `.obsidian/snippets/` automatically. To install them manually, download your theme(s) of choice from the tables below, open Obsidian **Settings → Appearance → CSS snippets**, click the folder icon, drop the `.css` file(s) inside, refresh, and toggle the snippet on. **Only use one theme at a time.**

### Integrations
- This repository is structured to work with the **[Statblock Template Installer for Atlas](https://community.obsidian.md/plugins/statblock-template-installer-for-atlas)** community plugin by `@young_george` from the Discord.

---

# Downloads

## Automatic Installation (Recommended)
If you use the **[Statblock Template Installer for Atlas](https://community.obsidian.md/plugins/statblock-template-installer-for-atlas)** community plugin, you can install and update the template, layout snippet, and themes in one step:
1. Open Obsidian **Settings → Statblock Template Installer for Atlas**.
2. Click the **`+`** button next to **Templates**.
3. Paste this repository URL and click **Install** *(update `<REPO-NAME>` if you name the repository differently)*:
   ```text
   https://github.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet
   ```
4. All `.atlastemplate` files will be installed into `atlas-vtt/statblock-templates/`, and all `.css` files will be placed into `.obsidian/snippets/` (disabled by default; enable `wod-sheet-polish.css` and **one** theme under **Settings → Appearance → CSS snippets**).
5. To check for updates later, click the **refresh (`↻`)** icon in the plugin's settings tab.

*(Note: If you previously installed files manually under different filenames, delete the old files before running the plugin so you don't end up with duplicates.)*

## Manual Downloads
> **How to download individual files:** Click **View** on any file below and press the **Download raw file** button (the downward arrow icon in the top-right corner of the code box), or right-click **Download** and choose **Save Link As...**. If you want everything at once, grab the ZIP from the [Releases](https://github.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/releases) page on the right sidebar.

### Statblock Templates
Place inside `<Your Vault>/statblock-templates/` (or `<Your Vault>/atlas-vtt/statblock-templates/`).

| Template | Ruleset | View File | Direct Download |
| :--- | :--- | :--- | :--- |
| **World of Darkness (5e) Universal** | WoD5 | [World-of-Darkness-Character-Sheet.atlastemplate](World-of-Darkness-Character-Sheet.atlastemplate) | [Download](https://raw.githubusercontent.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/main/World-of-Darkness-Character-Sheet.atlastemplate) |

### Functional Layout Snippets (Recommended)
Place inside `<Your Vault>/.obsidian/snippets/` and toggle on in **Settings → Appearance → CSS snippets**. You can enable these alongside any visual theme.

| Snippet | Purpose | View File | Direct Download |
| :--- | :--- | :--- | :--- |
| **WoD5 Sheet Polish** | Adds Arena row labels, attribute names, and clickable 5-dot pip bars to the 3×3 Attribute table, aligns Skills/Trackers, and styles power/weapon cards | [World-of-Darkness-sheet-polish.css](World-of-Darkness-sheet-polish.css) | [Download](https://raw.githubusercontent.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/main/wod-sheet-polish.css) |
| **Two-Column Hover Preview** | Forces token hover previews in scenes to render in two columns | [two-column-hover.css](two-column-hover.css) | [Download](https://raw.githubusercontent.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/main/two-column-hover.css) |

### Visual Themes (Optional; enable only one)
Place inside `<Your Vault>/.obsidian/snippets/` and enable **one** theme at a time.

| Theme | Aesthetic | View File | Direct Download |
| :--- | :--- | :--- | :--- |
| **5e Parchment** | Classic vellum & crimson ink | [5e-parchment.theme.css](5e-parchment.theme.css) | [Download](https://raw.githubusercontent.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/main/5e-parchment.theme.css) |
| **Astral** | Navy & celestial gold | [astral.theme.css](astral.theme.css) | [Download](https://raw.githubusercontent.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/main/astral.theme.css) |
| **Crystal** | Indigo & violet/cyan (suggested by `@catapulttv` in the Discord) | [crystal.theme.css](crystal.theme.css) | [Download](https://raw.githubusercontent.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/main/crystal.theme.css) |
| **Gilded Obsidian** | Matte black & gold foil | [gilded-obsidian.theme.css](gilded-obsidian.theme.css) | [Download](https://raw.githubusercontent.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/main/gilded-obsidian.theme.css) |
| **Gothic** | Crimson & dark filigree *(recommended for Vampire / WoD)* | [gothic.theme.css](gothic.theme.css) | [Download](https://raw.githubusercontent.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/main/gothic.theme.css) |
| **Ice** | Glacial & cyan fractures | [ice.theme.css](ice.theme.css) | [Download](https://raw.githubusercontent.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/main/ice.theme.css) |
| **Infernal** | Fiery ash & ember orange | [infernal.theme.css](infernal.theme.css) | [Download](https://raw.githubusercontent.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/main/infernal.theme.css) |
| **Modern Blue** | Sci-fi circuit traces & sky-blue HUD | [modern-blue.theme.css](modern-blue.theme.css) | [Download](https://raw.githubusercontent.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/main/modern-blue.theme.css) |
| **Steampunk** | Riveted iron boilerplate & warm brass gears | [steampunk.theme.css](steampunk.theme.css) | [Download](https://raw.githubusercontent.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/main/steampunk.theme.css) |
| **Sylvan Woodcraft** | Forest bark, mossy stones & roots | [sylvan-woodcraft.theme.css](sylvan-woodcraft.theme.css) | [Download](https://raw.githubusercontent.com/ctrlaltransom/AtlasVTT-World-of-Darkness-Character-Sheet/main/sylvan-woodcraft.theme.css) |

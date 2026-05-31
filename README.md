# ⚔ Tank Battle

A browser-based tank combat game inspired by the classic Battle City. **Zero dependencies — just a single HTML file.** Open it and play.

## Features

- **3 game modes** — Campaign (8 levels), Custom (sliders + editor), Endless (escalating waves)
- **1P solo / 2P co-op** — shared lives, independent respawn
- **9 Power-ups** — Shield, Freeze, Fortress, Firepower (3 tiers), Extra Life, Bomb, Speed, Rapid Fire, Repair
- **3 enemy types** — Normal, Fast (blue/cyan), Heavy (gray, 2 HP)
- **6 terrain types** — Brick, Steel, Water, Trees, Ice, Base
- **Built-in terrain editor** — paint tiles, undo (Ctrl+Z), clear all, restore, save/load maps to localStorage
- **Spawn protection** — toggleable shield with configurable duration
- **Bullet modes** — Collide (bullets cancel each other) / Pierce (bullets pass through)
- **Web Audio sound effects** — fire, explosion, power-up, win/lose (toggleable)
- **Stats tracking** — elapsed time, kills, accuracy on game over
- **i18n** — 12 languages: English, 中文, 日本語, 한국어, Español, Français, Deutsch, Русский, Português, Italiano, ภาษาไทย, Tiếng Việt

## Controls

| Action  | Player 1     | Player 2 |
|---------|-------------|----------|
| Move    | W/A/S/D     | Arrows   |
| Fire    | Space       | Enter    |
| Pause   | P / Escape  | P / Escape |
| Edit    | E           | —        |
| Undo    | Ctrl+Z      | —        |

- **Start / Resume** — Enter
- **Click to advance** after clearing a level

## Game Modes

### Campaign
8 premade levels with 10–20 enemies each. Level-select UI shows completed stages.

### Custom
Adjust enemy count (1–30), fast enemies (0–10), and heavy armor enemies (0–10). Use the built-in terrain editor to design your own map, then start the battle.

### Endless
Wave-based survival on the current map. Enemies per wave = `5 + wave × 2`. Fast/Heavy chances and spawn speed increase with each wave.

## Terrain Types

| Type   | Visual | Collision |
|--------|--------|-----------|
| Brick  | Brown gradient with mortar | Bullets destroy a single brick |
| Steel  | Metallic gray with rivets | Indestructible (destroyable with Star×3) |
| Water  | Animated blue waves | Blocks tanks, bullets pass over |
| Trees  | Green canopy overlay | Visual only — tanks/bullets pass through |
| Ice    | Frosted white | Reduces friction, tanks slide |
| Base   | Blue icon polygon | Game over if destroyed |

## Power-ups

Spawn every 5 kills, last 8 seconds on the field.

| Icon | Name | Effect |
|------|------|--------|
| 🛡  | Shield | Invincibility for 10 s |
| ⏱  | Freeze | Freezes all enemies for 10 s |
| 🏰 | Fortress | Builds steel walls around base |
| ⭐  | Star | Upgrades firepower (max 3 — can destroy steel) |
| ❤  | Life | +1 extra life |
| 💥  | Bomb | Destroys all on-screen enemies |
| ⚡  | Speed | Doubles movement speed for 10 s |
| 🔥  | Rapid Fire | Halves shoot cooldown for 10 s |
| 🔧 | Repair | Restores all brick walls from original state |

## Map Editor

Press **E** (in menu or during play) to toggle the editor.

- **Left-click**: place selected terrain
- **Right-click**: erase
- **Scroll wheel**: cycle brush types
- **Ctrl+Z**: undo last paint
- **Clear All**: wipe the entire map
- **Restore**: revert to the saved pre-battle map
- **Save Map / Load**: persist custom maps in localStorage (Custom mode only)

Trees can be painted as a visual overlay on any terrain type — collision logic ignores them.

## Settings

Accessible via the ⚙ button in the sidebar.

- **Bullet Mode**: Collide (opposing bullets cancel) / Pierce (bullets pass through)
- **Spawn Shield**: Toggle player/enemy invincibility on spawn
- **Duration**: 1–10 seconds

## How to Run

1. Open `index.html` in any modern browser (Chrome, Firefox, Edge, Safari).
2. No server, no build step, no `npm install` — it just works.

## Disclaimer
This is a fan project created for educational and personal-use purposes. Inspired by Battle City (Namco, 1985). All original trademarks belong to their respective owners.

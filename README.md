# Dungeon Crawler — Procedural Roguelike

A fully featured browser-based roguelike dungeon crawler built in vanilla HTML, CSS, and JavaScript. No frameworks. No dependencies. Just a canvas, a grid, and a lot of dungeon.

**[▶ Play Live](https://krishnasingh-09.github.io/dungeon-crawler)**

---

## Features

### Procedural generation
- Every floor is uniquely generated using randomized BSP-style room placement
- Rooms connected by L-shaped corridors
- Staircase placed in the farthest room from the start

### Fog of war
- Raycasting field-of-view system (360° rays, radius 7)
- Explored tiles stay visible but dim when out of sight
- Enemies and items only visible within FOV

### Combat & RPG systems
- Bump-to-attack turn-based combat
- ATK vs DEF damage calculation with variance
- XP and leveling — each level boosts HP + ATK
- Equipment system — weapons and armor replace each other on equip

### Enemies (5 tiers)
| Symbol | Name | Notes |
|--------|------|-------|
| `g` | Goblin | Weak, fast XP |
| `s` | Skeleton | Armored |
| `O` | Orc | Strong melee |
| `T` | Troll | Tank |
| `D` | Dragon | Boss-tier, rare |

Enemies scale with floor depth and chase the player when in sight range.

### Loot
- Health potions (auto-use on pickup)
- Weapons: short sword, long sword
- Armor: leather, chain mail
- Gold drops from enemies and chests

### UI
- Live message log (color-coded: green = good, red = bad, yellow = loot, blue = info)
- Inventory panel showing equipped gear
- Stat bar: HP / ATK / DEF / XP / Level / Gold
- On-screen WASD controls for touch/mouse

---

## Controls

| Key | Action |
|-----|--------|
| `W` / `↑` | Move up |
| `S` / `↓` | Move down |
| `A` / `←` | Move left |
| `D` / `→` | Move right |
| Bump enemy | Attack |
| Walk over item | Pick up / equip |
| Walk onto `>` | Descend floor |

---

## Run Locally

No build step — just open the file:

```bash
git clone https://github.com/krishnasingh-09/dungeon-crawler.git
cd dungeon-crawler
open index.html
```

---

## License

MIT — free to use, remix, and build on.

# 東方幻夢郷 ～ Phantasmal Dream Land

A PC-98–style Touhou fan bullet-hell game built with vanilla HTML5 Canvas.  
No server, no dependencies — open `index.html` in any modern browser. or the attached pages link

---

## File Structure

```
touhou_game/
├── index.html
└── assets/
    ├── sprites/
    │   ├── player.png         (32×40)    – player ship
    │   ├── enemy_a.png        (24×24)    – small fairy
    │   ├── enemy_b.png        (28×28)    – mid fairy
    │   ├── enemy_c.png        (32×32)    – armoured enemy
    │   ├── boss_reimu.png     (48×56)    – Stage 1 & 5 boss
    │   ├── boss_marisa.png    (48×56)    – Stage 2 boss
    │   ├── boss_cirno.png     (48×56)    – Stage 3 boss
    │   ├── boss_yukari.png    (56×64)    – Stage 4 boss
    │   └── boss_sakuya.png    (48×56)    – Stage 6 boss
    ├── backgrounds/
    │   ├── bg1.png   – Grassy fields
    │   ├── bg2.png   – Ocean, islands
    │   ├── bg3.png   – Frozen desert
    │   ├── bg4.png   – Sky & clouds
    │   ├── bg5.png   – Leaving Earth
    │   └── bg6.png   – Deep space
    ├── palettes/
    │   └── level1–6/
    │       └── enemy_a/b/c.png  – level-tinted enemy sprites
    └── music/
        ├── title/title.mp3
        ├── level 1/stage.mp3  &  boss.mp3
        └── level 2–6/ …
```

---

## Controls

### PC (Keyboard)
| Key | Action |
|-----|--------|
| Arrow Keys | Move |
| **Z** | Shoot / Confirm menu |
| **X** | Bomb / Back in menu |
| **Shift** | Focus (slow + visible hitbox) |
| **ESC** or **Z** | Pause / Unpause |

### Mobile (Touch)
- **Virtual joystick** — touch anywhere on the left half of the screen; drag to move
- **FIRE** — shoot
- **FOCUS** — focus mode; placed next to FIRE for easy two-thumb use
- **BOMB** — screen-clearing bomb
- **⏸** — pause
- Multi-touch supported — all buttons are independent

### Both Platforms
- **⌂** (top-left) — return to title mid-game (saves hi-score)
- **⛶** (top-right) — toggle fullscreen
- Menu screens support arrow-key / D-pad navigation; Z confirms, X goes back

---

## Game Modes

| Button | Stages | Notes |
|--------|--------|-------|
| ▶ HARD MODE | 1–6 | Full difficulty |
| ☆ NORMAL MODE | 1–6 | Fewer / slower bullets; stage passwords available |
| ✿ BABY MODE | 1–6 | 5 lives, simpler patterns; stage passwords available |

---

## Stages & Bosses

| Stage | Theme | Boss |
|-------|-------|------|
| 1 | Grassy Fields | 博麗 霊夢 Hakurei Reimu |
| 2 | Ocean / Islands | 霧雨 魔理沙 Kirisame Marisa |
| 3 | Frozen Desert | チルノ Cirno |
| 4 | Sky / Clouds | 八雲 紫 Yakumo Yukari |
| 5 | Leaving Earth | 博麗 霊夢 Hakurei Reimu II |
| 6 | Deep Space | 十六夜 咲夜 Izayoi Sakuya |

---

## Power Levels

| Power | Shot type |
|-------|-----------|
| 1.0 | Single centre stream |
| 1.5 | Double stream |
| 2.5 | Double + straight side orbs |
| 3.5 | Double + purple homing orbs |

---

## Boss Fight Mechanics

- **Bosses 4–6**: slide to the left side, fire a homing stream, then return to centre
- **Stage 3 / Cirno**: periodically freezes time — player bullets stop, boss keeps attacking
- **Stage 6 / Sakuya**: below 50% HP, sweeps 6 laser charges across the full screen
- **Defeat screen**: boss quote plays, auto-advances after 3 seconds

---

## Passwords

### Title Screen (ENTER CODE box)
| Code | Effect |
|------|--------|
| Stage codes | Jump to a stage in Normal or Baby mode |

Stage codes appear on the stage banner for 4 seconds after each boss is defeated.  
Normal and Baby mode generate different codes for the same stage.

---


- **Mode** — Baby / Normal / Hard
- **Stage** — 1–6
- **Lives** — 1–7 or ∞ infinite lives
- **Power** — 1.0 / 1.5 / 2.5 / 3.5 / 4.0

---

## Music Room

Accessible from the title screen. Stage and boss themes for all 6 stages.  
Some tracks may be locked — play the game to find out how to unlock them.

---

## Hi-Score System

Scores saved to `localStorage` per mode.  
Title screen shows all current hi-scores.  
The ⌂ home button mid-run still saves your score.

---

## Buggy Mobile Support

- **Portrait mode**: "Rotate Device" overlay — game requires landscape
- **Fullscreen**: ⛶ button top-right
- **Virtual joystick**: appears wherever your thumb lands on the left half
- Buttons are DPI-scaled for consistent physical size across devices

---

## Adding Music

Place MP3 files matching the paths in the file structure above.  
Music crossfades between stage and boss tracks automatically.  
Missing files are silently ignored.

---

## Replacing Sprites

Drop any RGBA PNG into `assets/sprites/` using the same filename.  
The engine falls back to a solid-colour rectangle if an image fails to load.

---

> There may be more to this game than what's listed here.  
> Check the comments in `index.html` if you're curious.

## Credits

Fan project — not affiliated with Team Shanghai Alice / ZUN.  
Touhou Project © ZUN.

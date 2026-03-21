# 東方幻夢郷 ～ Phantasmal Dream Land

A PC-98–style Touhou fan bullet-hell game built with vanilla HTML5 Canvas.

```
touhou_game/
├── index.html
└── assets/
    └── sprites/
        ├── player.png       (32×40)   – shrine maiden ship
        ├── enemy_a.png      (24×24)   – small fairy
        ├── enemy_b.png      (28×28)   – mid fairy
        ├── enemy_c.png      (32×32)   – armoured enemy
        ├── boss_reimu.png   (48×56)   – Stage 1 boss
        ├── boss_marisa.png  (48×56)   – Stage 2 boss
        ├── boss_sakuya.png  (48×56)   – Stage 3 boss
        └── boss_yukari.png  (56×64)   – Stage 4 boss
```

## How to play

Open `index.html` in any modern browser — no server required.

| Key | Action |
|-----|--------|
| Arrow Keys | Move |
| **Z** | Shoot |
| **X** | Bomb (clears bullets) |
| **Shift** | Focus mode (slow + visible hitbox) |
| **ESC** | Pause |

## Replacing sprites

Drop any PNG with a transparent background into `assets/sprites/` using the
same filename. Recommended sizes are listed above, but the game scales to
whatever dimensions you use — just keep them roughly square for enemies and
portrait for the player / bosses.

The engine falls back to a solid-colour rectangle if an image fails to load,
so the game is always playable even with missing assets.

## Features

- 4 stages, each ending with a named boss
- 3 enemy types with different bullet patterns (aimed, spread, ring, spiral, laser)
- Multi-phase boss AI (patterns escalate as HP drops)
- Power-up / point-item pickups
- Graze scoring system
- Invincibility frames after being hit
- Bomb screen-clear with 3 charges
- Pixel-art sprites, scrolling starfield, PC-98 colour palette

## Credits

Fan project — not affiliated with Team Shanghai Alice / ZUN.  
Touhou Project © ZUN.

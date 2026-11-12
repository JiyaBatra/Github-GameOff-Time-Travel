<div align="center">

# Time Traveler: Space to Today

**A time-travel arcade game about recovering the cores that hold history together.**

![HTML5](https://img.shields.io/badge/HTML5-Canvas-e34f26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-f7df1e?logo=javascript&logoColor=black)
![No Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)
![Mobile Friendly](https://img.shields.io/badge/mobile-friendly-blue)

</div>

---

## About

**Time Traveler** is a lightweight 2D arcade-puzzle game built with plain HTML, CSS and JavaScript (Canvas). You travel from deep space through the lava age of early Earth, the age of dinosaurs and the tribal age, all the way to a futuristic colony. Each age has its own world, tasks, hazards, puzzle and wardrobe.

There are no frameworks, no build step and no server. It runs entirely in the browser.

## Features

- **5 unique ages**, each with its own background art, collectibles and hazards
- **SHIFT in Deep Space**: reverse gravity, draw nearby cores into your field, and send debris back
- **Combo scoring**: chain core pickups before the timer runs out to increase your score
- **Task + puzzle gameplay**: catch items to hit your goal, then solve a puzzle for bonus points
- **Wardrobe system**: 15 outfits (3 per age), each with a gameplay perk
- **Points economy**: earn points in every level and spend them on outfits
- **Free starter outfit**: the Space Suit is free, everything else must be bought
- **Auto-save**: points, owned outfits and progress are stored in the browser (`localStorage`)
- **Touch and mouse controls**: playable on phones, tablets and desktops
- **Fully offline**: no external requests or libraries

## How to Play

1. Press **Play** and open the **Wardrobe**.
2. Pick (or buy) an outfit for the current age, then press **Start**.
3. **Drag your finger or mouse** to steer. In Deep Space, press the on-screen **SHIFT** button, **Shift**, or **X** (gamepad **A**) to reverse gravity and pull nearby cores toward you.
4. Collect the time-cores and avoid debris. You have 3 lives (4 with a *Life* outfit).
5. Reach the item goal to unlock the core puzzle. Memory sequences get longer and faster in later ages. Matching puzzles give a brief layout preview, then add pairs, a countdown, and a limited number of mistakes. A failed attempt can be retried without losing the run score.
6. Spend your points on outfits for the next age and keep travelling forward in time.

### Scoring

| Action | Points |
| --- | --- |
| First pickup in a chain | 10 |
| Consecutive pickups | +10 per combo step, up to x5 |
| Puzzle completed | +30 |
| Outfit with *Bonus* perk | x1.5 on the level total |

## The Five Ages

| # | Age | Goal | Collect | Avoid | Puzzle |
| --- | --- | --- | --- | --- | --- |
| 1 | Deep Space | 8 items | Stars, oxygen cells | Asteroids | 5-signal memory sequence |
| 2 | Young Earth: Lava Age | 10 items | Water drops, crystals | Fire, rocks | 6 pairs · 50 seconds · 3 misses |
| 3 | Age of Dinosaurs | 12 items | Eggs, meat | Dinosaurs | 7-signal memory sequence |
| 4 | Tribal Age | 14 items | Fruit, wood | Snakes, boars | 8 pairs · 42 seconds · 2 misses |
| 5 | Future Colony | 16 items | Energy orbs, bolts | Robots, UFOs | 9-signal memory sequence |

### Game Off 2026: SHIFT

The Continuity Engine is breaking apart across time. In Deep Space, shifting gravity reverses the flow of stars, oxygen cells, and asteroids. The field also pulls nearby cores toward the player, making SHIFT a choice about when to take a risk for a pickup. The other ages retain their original catch-and-dodge loop while their distinct SHIFT mechanics are developed.

## Wardrobe

Every outfit has one of three perks:

- **Life**: +1 extra life
- **Magnet**: larger pickup range
- **Bonus**: x1.5 points for the level

| Age | Outfit (Cost, Perk) |
| --- | --- |
| 1. Deep Space | Space Suit (Free) · Neon Suit (40, Life) · Gold Suit (80, Bonus) |
| 2. Lava Age | Heat Suit (40, Life) · Rock Armor (60, Magnet) · Obsidian Cloak (90, Bonus) |
| 3. Dinosaur Age | Explorer (50, Life) · Camo Gear (70, Magnet) · Ranger (100, Bonus) |
| 4. Tribal Age | Leaf Wrap (50, Life) · Fur Cloak (70, Magnet) · Chief Feathers (100, Bonus) |
| 5. Future Colony | Cyber Wear (60, Life) · Android Armor (90, Magnet) · Star Commander (120, Bonus) |

> You must own at least one outfit of the current age to enter it. If you cannot afford one, replay the previous age to earn more points.

## Project Structure

```
.
├── index.html              # Game (HTML + CSS + JS in a single file)
├── README.md
└── assets/
    ├── backgrounds/        # Level backgrounds and star field (.jpg)
    │   ├── bg1_space.jpg
    │   ├── bg2_lava.jpg
    │   ├── bg3_dinosaur.jpg
    │   ├── bg4_tribal.jpg
    │   ├── bg5_future.jpg
    │   └── bg_starfield.jpg
    └── characters/         # 15 outfit images, transparent (.webp)
        ├── 1_space_suit.webp  ...  5_star_commander.webp
```

All asset paths are **relative** (for example `assets/characters/1_space_suit.webp`), so the project works from any folder or GitHub Pages sub-path without changes.

## Run Locally

No installation required.

1. Download or clone the repository.
2. Keep `index.html` and the `assets/` folder together.
3. Open `index.html` in any modern browser.

## Deploy on GitHub Pages

1. Push `index.html`, `README.md` and the `assets/` folder to the **root** of your repository.
2. Go to **Settings → Pages**.
3. Under *Build and deployment*, choose **Deploy from a branch**.
4. Select branch `main` and folder `/ (root)`, then press **Save**.
5. Your game will be live at `https://<username>.github.io/<repository>/`.

## Customization

- **Replace art**: overwrite any file in `assets/` with a new image of the same name.
- **Edit levels, goals and items**: change the `L` array at the top of the script in `index.html`.
- **Edit outfit prices and perks**: change the `O(...)` entries inside each level's `o` list.
- **Reset progress**: use the **Restart** button on the main menu, or clear the site data in your browser.

## Tech Stack

- HTML5 Canvas for rendering
- Vanilla JavaScript (no libraries)
- CSS with a responsive, touch-friendly layout
- `localStorage` for saving progress

## Credits

Replace this section with the sources and licenses of your artwork before publishing.

## License

Add a license of your choice here (for example MIT) before sharing the repository publicly.

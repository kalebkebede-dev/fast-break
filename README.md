# Fast Break 🏀

A 3D endless runner on a basketball court, made with Three.js.

**Play it here:** https://kalebkebede-dev.github.io/fast-break/ (works on desktop and phones)

![Fast Break gameplay](docs/gameplay.png)

## What it is

You're the ball on a fast break, and the court keeps scrolling at you. Red defenders block a lane, so you have to switch around them. White screens are low, so you jump over them. Blue orbs give bonus points, and grabbing 10 in a row bumps up your multiplier (max x8). The game keeps speeding up until you turn it over.

I wanted to try 3D in the browser without a game engine, so this is plain JavaScript and Three.js in one HTML file.

## Controls

- A / D or arrow keys: switch lanes (swipe on mobile)
- W, Space or Up: jump (swipe up or tap on mobile)

## How it works

- **Game loop.** It uses `requestAnimationFrame`, with delta time capped so a laggy frame doesn't make the ball teleport through things.
- **Fair spawning.** Every row of obstacles always leaves at least one lane open, so you never get a row you can't get past. As the speed goes up, the rows also get closer together.
- **Collisions.** These are simple distance checks, but defenders and screens behave differently: you can jump a screen but not a defender.
- **No image files.** The hardwood floor and the ball texture are drawn with the Canvas API at runtime and then used as textures.
- **Mobile.** Swipes and taps call the same functions as the keyboard, so both play the same way.

## Running it yourself

Just open `index.html` in a browser. There's nothing to install.

## What I want to add next

- [ ] Power-ups (shield, slow-mo)
- [ ] Sound effects and music
- [ ] Pause menu and difficulty settings

## Credits

I built the first prototype with help from Claude as an AI pair programmer. The commit history shows what was added when.

MIT License

# Fast Break

A 3D endless runner built with Three.js. A basketball rolls down a scrolling court while you dodge defenders, jump low screens, and collect orbs to build a score multiplier.

## Play
Open `index.html` in any modern browser. No build step or install is needed.

## Controls
- **A / D** or **arrow keys**: switch lanes (swipe left or right on mobile)
- **W / Space / Up**: jump (swipe up or tap on mobile)

## Rules
- Defenders (red) block a lane, so switch lanes to get past them
- Screens (white) are low, so jump over them
- Orbs add 25 × your multiplier; every 10 collected in a row raises the multiplier (max x8)
- Speed ramps up over time and rows get closer together
- Best score saves in the browser

## How it works
- **Game loop:** `requestAnimationFrame` with a capped delta time so slow frames don't break physics
- **Movement:** smoothed lane switching plus a gravity-based jump arc
- **Spawner:** every row leaves at least one lane open, so every row is passable, and the gap between rows shrinks as speed increases
- **Collision:** distance checks per object type; screens can be cleared by jumping, defenders cannot
- **Graphics:** court and ball textures are generated with the Canvas API, so the game ships as a single HTML file with no image assets

## Ideas to extend
- Power-ups such as a shield or slow-motion
- Sound effects and music
- Pause menu and difficulty settings

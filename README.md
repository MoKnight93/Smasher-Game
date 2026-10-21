# Smasher

A fun, cartoony, desktop-only web game. Smash bugs, smash your own logos, or beat up a goofy ragdoll buddy with a huge arsenal of silly weapons. No blood, no installs, no dependencies: it's a single `index.html` file.

> Just open `index.html` in a modern desktop browser (Chrome, Edge, Firefox) and play.

## Game modes

| Mode | What it is |
|------|-----------|
| ⭐ **Score** | Targets cross the screen from one edge to the opposite one. Smash them before they escape. You have 5 lives and it gets harder as your score grows. |
| ♾️ **Endless** | No score, no lives. Just smash forever. |
| 🥊 **Buddy** | A ragdoll to beat up. His head is your logo if you picked one, otherwise a normal cartoon head. Cartoon damage only. |

By default the targets are colorful cartoon spiders. You can swap them for **your own logos** (see below).

## Controls

| Input | Action |
|-------|--------|
| **Left click** | Use the current weapon (hold for flame, spray, vacuum, laser sword) |
| **Mouse wheel** / **Q** / **E** / **← →** | Change the weapon in the active slot |
| **1** | Select the normal weapon slot |
| **2** | Arm the ultra slot (click once to fire, then it recharges) |
| **Hover a slot** | Open the full weapon list and click one |
| **Right click + drag** *(Buddy)* | Grab and throw the buddy |
| **F** *(Buddy)* | Get a fresh buddy |
| **H** *(Buddy)* | Next logo head |
| **P** | Back to menu |
| **R** | Restart |
| **M** | Mute |

## Weapons

**Normal (9):** Shoe, Swatter, Flamethrower, Hammer, Zapper, Shotgun, Bug Spray, Vacuum, Laser Sword.

**Ultras (6):** Freeze, Black Hole, RPG, TNT, Giant Cat, Lightning Storm. An ultra hits the whole screen, then you swap back to your normal weapon and it recharges.

Weapons interact with each other and with the buddy: flame ignites bug spray into a fireball, the laser sword slices limbs off the buddy, the shotgun blows holes in his clothes, the vacuum sticks him to the nozzle so you can drag him around, freeze turns him into an ice block that shatters, and so on.

## Use your own logos

Three ways:

1. In the menu click **🖼️ CHOOSE MY LOGOS** and pick images.
2. **Drag & drop** images onto the page.
3. Put images in a `logos/` folder next to `index.html` and list them at the top of the script:

   ```js
   const LOGO_FILES = ['./Assets/Images/logo.png', './Assets/Images/logo.svg'];
   ```

Click **🕷️ USE SPIDERS** to go back to the default spiders.

## Tech

- Plain HTML + CSS + JavaScript on a `<canvas>`. No libraries, no build step.
- Sounds are synthesized with the Web Audio API (no audio files).
- The buddy is a Verlet-integration ragdoll with distance constraints and posture springs.
- Settings (best score, selected weapons) are saved in `localStorage`.

## Notes

- Desktop only (it needs a mouse with a wheel and right button).
- This is a fan-made fun project. If you use logos you don't own, keep it for personal use.

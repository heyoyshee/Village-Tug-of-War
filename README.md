# 🌾 রশি টানাটানি — Village Tug of War

A fun, village-themed **tug of war** game that runs entirely in your browser. Team Red 🔴 faces Team Green 🟢 on a sunny rural field with huts, palm and banana trees, drifting clouds, and kites in the sky. Play solo against the AI or challenge a friend on the same device.

The interface is in **Bangla** (with some English), and the whole game lives in a single HTML file: no installation, no build step, no dependencies.

## Features

- **Two game modes**
  - **Single Player:** you play Team Red, the AI plays Team Green
  - **Local Multiplayer:** two players on one keyboard or one touch screen
- **Three AI difficulty levels:** Easy (সহজ), Normal (মধ্যম), Hard (কঠিন)
- **Best-of-3 matches:** first team to win 2 rounds is the champion
- **Stamina system:** every tap costs energy, so spamming without a plan makes you weaker; stamina regenerates over time
- **Rope physics:** momentum, damping and tension make the rope feel alive
- **Procedural sound effects** (Web Audio API): taps, rope creaks, whistles, and crowd cheers, with a mute button
- **Animated canvas scenery and characters** that lean back and pull as you tap
- **Responsive 16:9 layout** that works on desktop, tablet, and mobile

## How to Run

1. Download or clone the project:
   ```bash
   
   ```
2. Open `tug_of_war_village.html` in any modern browser (Chrome, Edge, Firefox, Safari).

That's it. No server required.

> **Note:** The Bangla fonts (Baloo Da 2 and Hind Siliguri) load from Google Fonts, so an internet connection gives the best look. Without it, the game still works with fallback fonts.

## How to Play

Pull the rope to your side until it crosses your team's win line. Tap or press your key **repeatedly**. Holding a key down does nothing, because each press counts as one pull.

### Controls

| Mode | Team Red (left) | Team Green (right) |
|------|-----------------|--------------------|
| Single Player | `Space` or the red on-screen button | Controlled by AI |
| Multiplayer | `A` or `Space` or the red button | `L` or the green button |

On touch devices, use the big round **টানো!** buttons at the bottom corners.

### Tips

- Keep an eye on the **stamina bar** at the top. When it hits zero, your pulls become much weaker.
- Short pauses let stamina recover. Rhythm beats button mashing.
- The dashed white lines on either side of the field mark the **win lines**.

## Game Rules

1. Each round starts with a **3-2-1** countdown and a whistle.
2. Pull the rope marker past your side's win line to win the round.
3. The first team to win **2 rounds** wins the match.
4. After the match, choose **আবার খেলো** (Rematch) or **মেনুতে ফিরে যাও** (Back to Menu).

## Tech Stack

- HTML5, CSS3, and vanilla JavaScript (no frameworks or libraries)
- HTML5 `<canvas>` for rendering
- Web Audio API for generated sound effects
- Google Fonts: Baloo Da 2, Hind Siliguri

## Project Structure

```
.

```

## Customization

Settings you can tweak in the JavaScript section of `tug_of_war_village.html`:

| What | Where |
|------|-------|
| AI speed and strength | `AI_PARAMS` (`easy`, `normal`, `hard`) |
| Rope distance needed to win | `WIN_THRESHOLD` |
| Pull strength and stamina cost | `doTap()` (`basePower`, `cost`) |
| Stamina regeneration speed | `updatePhysics()` (`regen`) |
| Rounds needed to win a match | `endRound()` (the `=== 2` checks) |

## Future Ideas

- Online multiplayer
- Team and character customization
- More village scenes and weather
- Power-ups and special moves
- High-score tracking

## License

Add your preferred license here (for example, MIT).

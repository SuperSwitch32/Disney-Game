# Disney Auction

Single-file pass-and-play Disney character auction game. Open `index.html` in any modern browser. That's it.

## How to play

1. **New Game** → add 2–6 players, pick a scoring mode, **Start**.
2. The device sits flat on a table. Each player has their own panel oriented toward their seat: their name, remaining budget, and a big **BID** button.
3. A random Disney character appears in the center with a countdown timer.
4. Tap **BID** to raise the price by $1. Every bid resets the timer.
5. When the timer hits 0, the leader wins the character.
6. After all rounds, the game ends with either **player voting** (each player votes for the best team, can't vote for themselves) or **character points** (popularity score based on films, shows, games, attractions).

## Settings

Tweak from the main menu → **Settings**:

- Budget per player (default $20)
- Characters per game (default 10)
- Starting bid (default $1)
- Bid increment (default $1)
- Initial timer (default 15s)
- Reset timer on bid (default 5s)

Settings are saved in `localStorage`.

## Layout

- **Phone**: 2–4 players (panels on each edge).
- **iPad / tablet**: comfortable up to 6 players.

## What gets auctioned

Two modes, picked on the setup screen:

- **Characters** — ~100 popular Disney / Pixar characters (Mickey, Elsa, Simba, Woody, Stitch, etc.). Images come from the [Disney API](https://disneyapi.dev/).
- **Park Attractions** — ~45 famous Disneyland and Walt Disney World rides (Space Mountain, Haunted Mansion, Rise of the Resistance, Flight of Passage, etc.). Images come from Wikipedia.

Each item has a hand-tuned popularity score used in the "Item points" scoring mode. If an image can't be loaded for a specific item, the stage shows the name as a fallback. Needs internet to start a new game.

To customize the rosters or point values, edit the `CURATED_CHARACTERS` and `CURATED_ATTRACTIONS` arrays near the top of the `<script>` block in `index.html`.

## Deploy

It's a single static HTML file — open locally, drop on GitHub Pages, Netlify drop, anywhere. No build step.

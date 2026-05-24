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

## Characters

Pulled live from the public [Disney API](https://disneyapi.dev/) — needs internet to start a game. Only characters with images and at least one film/show/game/attraction credit are used. Each character's point value is a weighted popularity score (films × 3 + tv shows × 2 + park attractions × 2 + short films + video games).

## Deploy

It's a single static HTML file — open locally, drop on GitHub Pages, Netlify drop, anywhere. No build step.

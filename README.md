# IMPOSTER

IMPOSTER is an Android-first local pass-and-play multiplayer social-deduction game. One player is secretly assigned as the Imposter each round, while every other player sees the secret word and category. Everyone discusses clues in real life, votes privately on one phone, and then reveals whether the group caught the Imposter.

> **One phone. One secret word. One Imposter. Can you find them?**

## Web version

This repository also contains a browser-native version for phones and desktop browsers. It uses HTML/CSS/JavaScript and does **not** require Python or Kivy in the browser.

### Deploy on Vercel

1. Import this repository into Vercel.
2. Framework preset: **Other** (or leave it as the detected static configuration).
3. Build command: leave empty.
4. Output directory: `.`.
5. Deploy.

The site is a static pass-and-play game, so no server or database is required. The original Python/Kivy implementation remains in the repository for Android/offline use.

## Run on Android with Python/Kivy

You can use any Python interpreter, IDE, or development environment that supports Python and Kivy. Pydroid 3 is recommended for the easiest setup on Android.

### Recommended: Pydroid 3

1. Install Pydroid 3 on Android.
2. Install Kivy support in Pydroid 3.
3. Download this repository and extract it.
4. Open `main.py` in Pydroid 3 and press Run.

## Game rules

- 👥 **3–10 players** play together on one device.
- 🎭 One player is secretly chosen as the Imposter.
- 🕵️ Everyone else receives the same secret word and category; the Imposter sees only the category.
- 📱 Pass the device around for private role reveals.
- 💬 Discuss clues in real life.
- 🗳️ Each player privately votes for the suspected Imposter.
- 📊 Votes are revealed.
- 🏆 The game reveals the Imposter, word, category, and round scoring.
- 🔄 **Play Again** starts another round with the same players.

## Project structure

```text
index.html              # Browser entry point
style.css               # Browser UI and responsive styling
app.js                  # Browser game state, screens, reveal, voting and scoring
main.py                 # Kivy app entry point
game/
  game_logic.py         # Original Python game logic
  word_database.py      # Original bilingual word/category data
screens/
  common.py
  main_menu.py
  reveal.py
  ready_vote.py
  voting.py
  vote_summary.py
  results.py
assets/main-menu/       # Player and pencil image assets
assets/screenshots/     # README screenshots
animations/
  screen_morph.py
```

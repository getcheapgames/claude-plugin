---
name: games-under-a-budget
description: Recommend the best-rated games in a genre, on a platform, under a price, as a table with ratings and prices. Use when someone asks for a game under a budget, such as "a strategy game under $20" or "a cheap RPG for Xbox".
---

# Recommend games under a budget

Use `find_games` from the getcheapgames tools.

1. Work out the genre (Steam's names: Action, Adventure, Casual, Indie, Massively Multiplayer, Racing, RPG, Simulation, Sports or Strategy), the platform (`pc`, `xbox`, `playstation` or `switch`) and the budget, in the reader's currency.
2. Call `find_games` with `genre`, `platform`, `max_price` and the reader's `country`. Five results is a good default.
3. The results are ranked by how popular and well rated each game is on Steam.

Answer with a table: the game (linked to its `pageUrl`), its Steam rating, and its lowest price on the platform asked for. Then one or two sentences on why the top picks stand out. If nothing fits the budget, say so and suggest raising it or trying another genre.

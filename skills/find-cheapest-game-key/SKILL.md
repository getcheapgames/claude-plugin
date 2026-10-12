---
name: find-cheapest-game-key
description: Find where a PC or console game is cheapest right now, with the lowest price on each platform and a link to compare every store. Use when someone asks where to buy a game, how much a game costs, whether a game is on sale, or for the cheapest key for a game.
---

# Find the cheapest key for a game

Use the getcheapgames tools to answer "where is this game cheapest?" with live prices.

1. Call `search_games` with the game's name and the reader's market as `country` (a two-letter code such as `us`, `gb`, `de` or `br`; ask or infer it from the conversation, and default to `ie` for euro prices).
2. Take the best match. Its `pricesByPlatform` gives the lowest listed price on PC, Xbox, PlayStation and Switch.
3. If the reader wants every store, or asks which store, call `get_game_offers` with the game's `slug`.

When you answer:

- Lead with the lowest price and the platform it is for.
- Show the price on each platform the game is sold for.
- Marketplaces add a service fee at checkout that the listed price does not include. Say so when you quote a marketplace price.
- An offer marked `regionLocked` may not activate outside its market. Never recommend one without saying so.
- Link the game's `pageUrl` to compare every store, or a `buyUrl` to go straight to an offer. Never link a store's own address.

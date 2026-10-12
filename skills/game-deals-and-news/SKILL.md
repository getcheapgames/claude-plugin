---
name: game-deals-and-news
description: Show today's biggest game deals and getcheapgames' latest news, buying guides and reviews. Use when someone asks what is on sale, for the best game deals today, for gaming news, or for a buying guide or review of a game.
---

# Show deals and news

For deals, call `list_deals` with the reader's `country`: the games where shopping around saves the most right now. Show each game with its lowest price per platform and link its `pageUrl`.

For news, guides and reviews, call `list_news` with the reader's `country`. Narrow it with `tag` (`news`, `guide`, `review`, `deals` or `video`) or search titles with `query`, such as "GTA 6". Show each post as a card: its cover image (`imageUrl`), title, summary and a link to its `url`.

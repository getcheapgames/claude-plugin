# getcheapgames for Claude

Find the cheapest legit key for any PC or console game, without opening a dozen store tabs. This plugin connects Claude to [getcheapgames](https://getcheapgames.com), which compares game key prices across official stores (Steam, GOG, the Nintendo eShop and others) and key marketplaces (G2A, Kinguin, Gamivo and others) in 40 markets, in each market's currency.

Ask Claude things like:

- "Where is Elden Ring cheapest right now?"
- "Find me a strategy game under $20."
- "Suggest a free-to-play action game for PC."
- "What are the best game deals today?"
- "Is there a buying guide for GTA 6?"

## What's included

- **Connector:** the getcheapgames MCP server at `https://mcp.getcheapgames.com`, with read-only tools to search games, list every offer for a game, list the biggest savings, find the best-rated games under a price, suggest free-to-play games, list a franchise's or publisher's games, list the compared stores, and read getcheapgames' news, guides and reviews.
- **Skills:** `find-cheapest-game-key`, `games-under-a-budget`, `free-to-play-games` and `game-deals-and-news`, which tell Claude how to use those tools and how to present the answers: prices per platform, region-lock warnings, tables and cards.

## What it sends and stores

The plugin runs no code on your machine. When Claude uses a tool, it sends the tool's arguments to `https://mcp.getcheapgames.com`: what you asked about (a game name, a genre, a budget, a platform) and a market code such as `us` or `de`. No account is needed, nothing about you is sent, and the tools only read public prices: they never buy anything or change anything.

The server limits how often it can be called, so a very busy session may be asked to wait a minute.

Links in the answers go to getcheapgames.com. Most links to stores are affiliate links: getcheapgames may earn a commission when you buy, which never changes the price you pay or the order offers are ranked in.

- Privacy policy: https://getcheapgames.com/ie/privacy
- How offers are ranked: https://getcheapgames.com/ie/how-we-rank

## Support

Questions, corrections or a price we have wrong: hello@getcheapgames.com.

## License

MIT. See [LICENSE](LICENSE).

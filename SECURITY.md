# Security policy

## What this covers

This repository holds the getcheapgames plugin: instructions and a connection to the getcheapgames MCP server at `https://mcp.getcheapgames.com`. The plugin runs no code on your machine.

The server is public and read-only. It needs no account, API key or token, it holds nothing about the people who use it, and its tools only read public game prices, news and store details: they never buy, write or change anything.

## Supported versions

Only the current version of the plugin and the live server are supported. Fixes go to the live server and to the `main` branch here.

## Reporting a vulnerability

Email **hello@getcheapgames.com** with "Security" in the subject, or use GitHub's private vulnerability reporting on this repository (Security tab, "Report a vulnerability").

Please include:

- what you found and where (the server, a tool, a link it returns, or a file in this repository),
- the steps or the request that show it,
- what someone could do with it.

Please do not open a public issue for a security problem, and do not test in ways that degrade the service for others: the server limits requests per caller.

We aim to reply within 3 working days, and to fix confirmed issues in the live server as soon as we can. We will tell you when it is fixed, and credit you if you would like.

## Out of scope

- Prices, availability or listings shown by third-party stores and marketplaces: report a wrong price to hello@getcheapgames.com as a normal correction.
- Rate limiting (HTTP 429) from normal use.

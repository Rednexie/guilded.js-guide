# 📚 Introduction

## Welcome to Guilded.js

Guilded.js is a library for the Guilded.gg API written in TypeScript. It is usable in either TypeScript or JavaScript project and is built to be customizable and extendable, perfect for both hobbyist programmers and those that need a library that will scale with their bot.

The library is heavily inspired by discord.js design-wise. We appreciate the work that they've done over there, [so go give them a star](https://github.com/discordjs/discord.js).

Guilded.js is made up of various sub-packages, allowing more seasoned programmers that only need certain functionalities to install only what they need. However, for most people, you will only ever need to install the main `guilded.js` package.

A quick overview of all the sub-packages:
> If you're new to the project, the following packages are likely what you're going to be using.
* `guilded.js` ([**GitHub**](https://github.com/guildedjs/guilded.js/tree/main/packages/guilded.js#readme)**,** [**NPM**](https://www.npmjs.com/package/guilded.js)) - The main library that ties everything together. Contains structures, caching, and other utilities for building your bot.
* `@guildedjs/gil` ([**GitHub**](https://github.com/guildedjs/guilded.js/tree/main/packages/gil#readme)**,** [**NPM**](https://www.npmjs.com/package/@guildedjs/gil)) - Our bot command framework, allowing you to skip a lot of the boilerplate needed to make most bots and jump straight into working on your commands.


> **Warning: These packages are meant for more seasoned programmers who know exactly what functionality they need. You will likely not need to import any of these as they're already included in the main package.**
* `@guildedjs/guilded-api-types` ([**GitHub**](https://github.com/guildedjs/guilded.js/tree/main/packages/guilded-api-typings#readme)**,** [**NPM**](https://www.npmjs.com/package/@guildedjs/guilded-api-typings)) - Raw typings for the guilded API, suitable for projects that want to interface directly with the API without having to write types of their own.
* `@guildedjs/webhook-client` ([**GitHub**](https://github.com/guildedjs/guilded.js/tree/main/packages/webhook-client#readme)**,** [**NPM**](https://www.npmjs.com/package/@guildedjs/webhook-client)) - Library agnostic client for send messages through Guilded webhooks.
* `@guildedjs/rest` ([**GitHub**](https://github.com/guildedjs/guilded.js/tree/main/packages/rest#readme)**,** [**NPM**](https://www.npmjs.com/package/@guildedjs/rest)) - Utility for making REST requests to the Guilded API. Includes rate-limiting, proxy support, and route utility functions
* `@guildedjs/ws` ([**GitHub**](https://github.com/guildedjs/guilded.js/tree/main/packages/ws#readme)**,** [**NPM**](https://www.npmjs.com/package/@guildedjs/ws)) - Utility for connecting to Guilded's WebSocket gateway and receiving events. Supports replaying events and handling disconnects.

> **This guide assumes that you have a basic understanding of JavaScript and Node.JS. If you don't, it's recommended that you start with learning that first, then proceeding with this guide.**

## Ready to get started?

Here are some of the articles that you're probably looking for.

[setting-up-a-guilded-bot.md](setting-up-a-guilded-bot.md)

[create-a-basic-bot.md](create-a-basic-bot.md)
{% endcontent-ref %}

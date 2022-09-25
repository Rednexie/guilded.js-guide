---
description: Let's create a basic pong bot!
---

# Create a basic bot

If you haven't created the bot application on Guilded or copied your bots auth token follow the below.

{% content-ref url="setting-up-a-guilded-bot.md" %}
[setting-up-a-guilded-bot.md](setting-up-a-guilded-bot.md)
{% endcontent-ref %}

## Create the bots main file

Let's create an `index.js` or `index.ts` file so that we can have our bot login!

{% tabs %}
{% tab title="JavaScript" %}
{% code overflow="wrap" %}
```javascript
// index.js
// Import the guilded client
const { Client } = require('guilded.js');

/**
 * Create an instance of the client class
 * To be even more secure use environment variables or a config.json!
 */
const client = new Client({
  token: 'your-super-secret-bot-token',
});

// When the bot connects successfully, log to the console.
client.on('ready', () => {
  console.log(`Bot is successfully logged in as ${client.user.name}`);
});

// Login to Guilded
client.login();

```
{% endcode %}
{% endtab %}

{% tab title="TypeScript" %}
```typescript
// index.ts
// Import the guilded client
import { Client } from 'guilded.js';

/**
 * Create an instance of the client class
 * To be even more secure use environment variables or a config.json!
 */
const client = new Client({
  token: 'your-super-secret-bot-token',
});

// When the bot connects successfully, log to the console.
client.on('ready', () => {
  console.log(`Bot is successfully logged in as ${client.user?.name}`);
});

// Login to Guilded
client.login();
```
{% endtab %}
{% endtabs %}

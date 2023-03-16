# Responding to messages

Now that you've created your bot and successfully started it for the first time, let's move on to having your bot respond to your messages!

Starting off, we have to listen to the [`messageCreated` ](https://github.com/guildedjs/guilded.js/blob/1780c2c/packages/guilded.js/lib/structures/Client.ts#L158)event, which emits a [`Message` ](https://guilded.js.org/classes/guilded\_js.Message.html)object.&#x20;

{% tabs %}
{% tab title="JavaScript" %}
{% code overflow="wrap" %}
```javascript
// index.js
// add this to your index.js file, preferably above the ready event listener

client.on("messageCreated", async message => {
     if(!message.content.startsWith("!")) return;
     // type 0 is for bots
     if (member.user.type === 0) return;
     
     if(message.content === "!hi") return message.reply("hi there!");
});
```
{% endcode %}
{% endtab %}

{% tab title="TypeScript" %}
{% code overflow="wrap" %}
```typescript
// index.ts
// add this to your index.ts file, preferably above the ready event listener

client.on("messageCreated", async message => {
     if(!message.content.startsWith("!")) return;
     // type 0 is for bots
     if (member.user.type === 0) return;
     
     if(message.content === "!hi") return message.reply("hi there!");
});
```
{% endcode %}
{% endtab %}
{% endtabs %}

Now, let's explain what this code does. Inside the event listener, we have an [asynchronous ](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async\_function)[arrow function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow\_functions). This allows us to resolve the [promises ](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Promise)returned by some of our method calls. Inside this function, the first thing we do is check whether the message starts with our prefix (we chose `!` for example). If it doesn't, then we ignore the message.&#x20;  

{% endhint %}

Finally, we do a simple string comparison to see whether the contents of the message match `!hi` exactly. If it does, the bot will reply to the author with the words `hi there!`. Congratulations, you have now created a bot that responds to messages!



### Some practice concepts for you

To help better your skills and prepare you for what's to come next, it's advised that you try the following out:

* Chaining your if statement with some else-if statements to have multiple commands.
* Using a switch-case statement to explore alternatives to else-if chaining.
* [Extracting the command name from the message](https://v12.discordjs.guide/command-handling/#command-handling) for a cleaner string comparison experience&#x20;

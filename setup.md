# Setting up

Make sure you have all the prerequisites listed here:

* [Deno](https://deno.land/) - Needed to run the bot
* [An application with a bot user](https://discord.com/developers/applications/) - Needed for obivious reasons. If you have not created one yet, make one now and add it to a test server.

Then make a new folder where your code will be.

In this folder, create a file. This will be the main file of your bot. Import the `CascadeClient` like this:

```typescript
import { CascadeClient } from "https://deno.land/x/cascade@1.0.6/mod.ts";
```

You then need to create the client as demonstrated below.

```typescript
import { CascadeClient } from ".https://deno.land/x/cascade@1.0.6/mod.ts";
import { join } from "https://deno.land/std@0.86.0/path/mod.ts";

const client = new CascadeClient({
    token: "Replace this with your token",
    commandHandlerOptions: {
        commandDir: join(Deno.cwd(), "commands"),
        prefix: "Replace this with your prefix"
    },
    listenerHandlerOptions: {
        listenerDir: join(Deno.cwd(), "listeners"),
    },
    inhibitorHandlerOptions: {
        inhibitorDir: join(Deno.cwd(), "inhibitors"),
    },
    owners: ["487443883127472129"], // Replace with the owners of the bot's ids
    verbose: true // Disable this if you don't want cascade to log things
});

await client.init();
await client.login();
```

This sets up the base for your bot, and is where it all starts. If you run it now, it will throw errors because it can't find the listeners, commands, and inhibitors directories. To fix this, create all of those. Then the bot should then run.

## Next steps

* [Commands](commands.md)
* [Listeners \(WIP\)](listeners.md)
* [Inhibitors \(WIP\)](inhibitors.md)


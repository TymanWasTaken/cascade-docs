# CascadeClient

This is the main entry point for all bots. It is how you set options for the bot and get cascade ready to be used.

```typescript
class CascadeClient
```

### Constructor

#### Usage:

```typescript
new CascadeClient(options: CascadeClientOptions)
```

#### Example:

```typescript
new CascadeClient({
    token: JSON.parse(await Deno.readTextFile("./test_config.json")).token,
    commandHandlerOptions: {
        commandDir: join(Deno.cwd(), "commands"),
        prefix: "ae!"
    },
    listenerHandlerOptions: {
        listenerDir: join(Deno.cwd(), "listeners"),
    },
    inhibitorHandlerOptions: {
        inhibitorDir: join(Deno.cwd(), "inhibitors"),
    },
    owners: ["487443883127472129"],
    verbose: true
});
```

{% hint style="info" %}
1. Verbose tells cascade if it should log or not. \(Turn this off if you already have logging or want to make your own\)
{% endhint %}


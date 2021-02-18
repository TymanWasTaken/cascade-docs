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
const client = new CascadeClient({
    token: 'token',
    commandHandler,
    listenerHandler,
    inhibitorHandler,
    owners: ["487443883127472129"],
    verbose: true
})
```

{% hint style="info" %}
1. This example assumes you have already created all of the handlers.
2. Verbose tells cascade if it should log or not. \(Turn this off if you already have logging\)
{% endhint %}


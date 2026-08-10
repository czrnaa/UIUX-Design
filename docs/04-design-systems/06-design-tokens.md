# Design Tokens

Suppose I tell you `Make this card's radius 8px.` That's a value.

But what if I instead tell you `Use radius-md.` Now we have a token.

```
radius-sm = 4px
radius-md = 8px
radius-lg = 16px
radius-full = 9999px
```

## Why bother?

Imagine your company decides *"Our UI feels too sharp. Increase our standard radius."*

Without a system:  You hunt through 70 screens.

With tokens:
- radius-md
- 8px → 10px

> ***The system changes.***
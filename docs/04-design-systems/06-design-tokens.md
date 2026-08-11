# Design Tokens

A design token is a named value representing a reusable design decision, such as a color, spacing, typography, or radius value. Basically giving it meaningful names for other members of the team or company to understand.

---

Imagine your file contains this color 400 times: `#2563EB`

Then the company your in rebrands.

*New primary: `#6750A4`*. Have fun changing 400 objects.

Instead, we introduce **abstraction**.

```
#2563EB
↓
blue-600
↓
color-action-primary
↓
Primary Button
```

These layers have different jobs.

|Types of Token|Description|
|--------------|-----------|
|Primitive token|blue-600, gray-900, space-4|
|Semantic token|color-action-primary, color-text-primary, color-surface-danger|

That's powerful because: `color-action-primary` could point to blue today and purple next year. **The meaning remains the same.**

In terms of programming, this might help you understand this:

|Token Type|Topic|Example|
|---------|--------|----|
|Primitive|Hardcoded|`background = #2563EB`|
|Semantic|Conceptually|`background = actionPrimary`|

> Same reason developers avoid magic values.

## Why bother?

Imagine your company decides *"Our UI feels too sharp. Increase our standard radius."*

Without a system:  You hunt through 70 screens.

With tokens:
- radius-md
- 8px → 10px

> *The system changes.*
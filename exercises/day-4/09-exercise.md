# Exercise 9

Create three frames:

```
Desktop — 1440
Tablet  — 768
Mobile  — 390
```

Don't immediately design all three independently.

## Desktop

```
Desktop — 1440

┌─────────────────────────────────────────┐
│ Logo                         Navigation │
│                                         │
│ Heading                                 │
│                                         │
│ [ Card ]    [ Card ]    [ Card ]       │
│                                         │
└─────────────────────────────────────────┘
```

### Then ask yourself what should happen with less space.

## Tablet

Perhaps tablet becomes:

```
Tablet — 768

┌──────────────────────────────┐
│ Logo              Navigation│
│                              │
│ Heading                      │
│                              │
│ [ Card ]       [ Card ]     │
│                              │
│ [ Card ]                    │
└──────────────────────────────┘
```

## Mobile

And mobile:

```
Mobile — 390

┌──────────────────┐
│ Logo          ☰  │
│                  │
│ Heading          │
│                  │
│ [     Card     ] │
│                  │
│ [     Card     ] │
│                  │
│ [     Card     ] │
└──────────────────┘
```

Now you're making design decisions, rather than merely resizing rectangles.

## Challenge

Make a simple card:

```
┌───────────────────────────┐
│                           │
│          IMAGE            │
│                           │
├───────────────────────────┤
│ Card title                │
│ Description               │
│                           │
│ [ Learn More ]            │
└───────────────────────────┘
```

- Build its contents with Auto Layout.
- Then repeatedly resize its parent.
- Watch for:
  - When does the text wrap?
  - When does the image become too narrow?
  - Does padding remain consistent?
  - Does the button need to grow?
  - Should the card have a minimum width?

## References

Personally, I'd watch this in order.

1. [Responsive Design with Auto Layout and Constraints in Figma
](https://www.youtube.com/watch?v=l47WcSwK1M0) - Javier Alaves
2.  [A practical guide to responsive web design
](https://www.youtube.com/watch?v=x4u1yp3Msao) - Kevin Powell

> I've also added my own input for this activity under the `answer-key/`
# Responsive Design

Responsive design is the practice of designing interfaces that adapt to different screen sizes and available space while remaining usable and visually organized.

Because a page might be viewed on:

```
Desktop          Tablet           Mobile
1440px           768px            390px

┌────────────┐    ┌────────┐       ┌──────┐
│ NAV        │    │ NAV    │       │ ☰    │
│            │    │        │       │      │
│ [] [] []   │    │ [] []  │       │  []  │
│ [] [] []   │    │ [] []  │       │  []  │
│            │    │        │       │  []  │
└────────────┘    └────────┘       └──────┘
```

Let's say you have a dashboard:

```
┌───────────────────────────────────────────┐
│ Sidebar │ Welcome, Alex                   │
│         │                                 │
│         │ Card    Card    Card            │
│         │                                 │
│         │ Recent Activity                 │
└───────────────────────────────────────────┘
```

Your task: **Make it mobile.**

```
Beginner:

Desktop
↓
shrink
↓
tiny desktop
```

To a professional? No.

### Ponder and Drop Questions

Ask: *"What does the mobile user need most?"*

Maybe:

```
┌─────────────────────┐
│ Orbit           ☰   │
│                     │
│ Welcome, Alex       │
│                     │
│ Card                │
│                     │
│ Card                │
│                     │
│ Recent Activity     │
│                     │
│ 🏠   📚   👤         │
└─────────────────────┘
```

## What can change?

As available width decreases:

|Desktop|Smaller screen|
|-------|--------------|
|4 cards in a row|2 cards → 1 card|
|Full navigation|Hamburger/menu|
|Sidebar + content|Sidebar hidden/moved|
|Large margins|Smaller margins|
|Horizontal sections|Vertical sections|
|Large images|Flexible/resized images|
|Multiple columns|Fewer columns|

### For Example

```
DESKTOP
┌─────────────────────────────────────────┐
│ Logo       Home  About  Shop     Login │
├─────────────────────────────────────────┤
│                                         │
│   [ Card ]   [ Card ]   [ Card ]       │
│                                         │
└─────────────────────────────────────────┘


MOBILE
┌─────────────────┐
│ Logo        ☰   │
├─────────────────┤
│                 │
│    [ Card ]     │
│                 │
│    [ Card ]     │
│                 │
│    [ Card ]     │
│                 │
└─────────────────┘
```

## Three concepts to understand

### 1. Flexible sizing

You've probably already encountered:

- Fixed
- Hug contents
- Fill container

These become very important now.

Imagine:

```
┌──────────────────────────────────────────┐
│ [Logo]                  [Search........] │
└──────────────────────────────────────────┘
```

If the search field has a fixed width of 600px, shrinking the parent can cause problems.

With flexible sizing, you can instead tell it:

```
Logo        → Hug / Fixed
Search      → Fill container
Parent      → Fill available width
```

Then:

```
Wide
[Logo] [================ Search ================]

Narrow
[Logo] [======= Search =======]
```

Figma's [<u>Auto Layout</u>](https://www.youtube.com/watch?v=1odqpkfkDL8) is specifically designed to let frames respond dynamically as their contents or available dimensions change, and it's available on all plans

### 2. Constraints

It answers the question:

*What should this element do when its parent frame changes size?*

#### For example:

```
┌──────────────────────────────────────┐
│ LOGO                          PROFILE│
└──────────────────────────────────────┘
```

You might want:

```
LOGO
Constraint → Left

PROFILE
Constraint → Right
```

Resize the parent:

```
Before:
| LOGO                         PROFILE |

After:
| LOGO              PROFILE |
```

> The profile remains attached to the right side.

Figma supports horizontal constraints such as Left, Right, Left and right, Center, and Scale.

#### One important distinction

Traditional constraints apply to children of regular frames; Auto Layout has its own resizing behavior, so don't think of constraints and Auto Layout as interchangeable.

### 3. Breakpoints

Sometimes a layout can't just keep shrinking.

Imagine: `[Logo] Home About Products Contact Login`

At some point: `[Logo] Home About Produc...` there isn't enough room.

Instead of continuing to squeeze everything, the design changes structure:

```
[Logo]                         ☰
```

- The widths where significant layout changes happen are commonly called breakpoints.
- Don't approach them as magical numbers you must memorize. 
- Think: *At what width does my current layout stop working well?*

Then design an appropriate response.

## Quick Exercise

Go to `exercises/day-4/09-exercise.md`
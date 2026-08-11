# Design Systems

This module introduces **Design Systems** and how they help designers create consistent, scalable, and reusable user interfaces.

Instead of designing every screen and component from scratch, a design system provides a shared collection of **foundations, styles, components, patterns, and guidelines** that can be reused throughout a product.

## What You'll Learn

By the end of this module, you should understand:

- What a design system is and why it matters
- How design systems improve consistency
- How to define colors and typography
- How to create a spacing system
- How to build reusable components
- How to use component variants and states
- How to organize components in Figma
- How design tokens work
- How designers and developers use the same design system

## Topics

### 1. Foundations

Learn the basic visual rules that establish the look and feel of a product.

Topics include:

- Colors
- Typography
- Spacing
- Grid and layout
- Border radius
- Shadows
- Icons

### 2. Design Tokens

Design tokens are reusable values that represent design decisions.

Instead of repeatedly using arbitrary values such as:

```text
Color: #1DB954
Spacing: 16px
Radius: 8px
```

we can give them meaningful names:

```text
color-primary
spacing-medium
radius-default
```

This makes designs easier to maintain and helps designers and developers stay consistent.

### 3. Components

Components are reusable UI elements that can be used across multiple screens.

Examples include:

- Buttons
- Inputs
- Cards
- Navigation bars
- Modals
- Dropdowns
- Tabs
- Badges

Instead of recreating these elements every time, we create them once and reuse them.

### 4. Variants and States

A single component may have multiple versions depending on its purpose or current state.

For example, a button could have:

```text
Button
├── Primary
├── Secondary
└── Destructive
```

It may also have different states:

```text
Default
Hover
Pressed
Focused
Disabled
```

Understanding these variations helps create interfaces that behave consistently.

### 5. Component Documentation

A good design system doesn't only contain components—it also explains **how and when to use them**.

Component documentation may include:

- Purpose
- Anatomy
- Variants
- States
- Usage guidelines
- Do's and don'ts
- Accessibility considerations
- Examples

## Why Design Systems Matter

Imagine designing a product with **50 different screens**.

Without a design system, you might accidentally use:

```text
Button A → 8px radius
Button B → 10px radius
Button C → 12px radius

Screen A → 20px padding
Screen B → 24px padding
Screen C → 18px padding
```

Small inconsistencies like these quickly accumulate.

With a design system, you establish rules:

```text
Button Radius → 8px

Spacing System
4px
8px
12px
16px
24px
32px
48px
```

Now every screen follows the same visual language.

> **Consistency reduces unnecessary design decisions and makes products easier to build, use, and maintain.**

## Key Takeaway

A **design system is more than a collection of components**. It is a shared set of rules and reusable building blocks that helps teams create consistent experiences across an entire product.

The goal isn't simply to make designs look the same—it is to make design decisions **intentional, reusable, and scalable**.

## Figma Link

Access and view my Figma Playground on Design Systems [<u>here</u> :)](https://www.figma.com/design/gICsJR3ZKJiOllS4sf5HRv/Design-Systems-Lab?node-id=4-11&p=f&t=YaZ3ph6yF3wZUBSq-0)
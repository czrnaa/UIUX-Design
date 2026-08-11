# Exercise 8

Build a 12-Column Desktop Grid

## 1. Create the desktop frame

  - Press: `F`. In the right sidebar, choose a desktop preset if available, or manually set:

    ```
    W: 1440
    H: 1024
    ```

  - Rename the frame:  `Desktop — 1440`

    You should now have:
    ```
    ┌──────────────────────────────────────────────────────┐
    │                                                      │
    │                  Desktop — 1440                      │
    │                                                      │
    │                                                      │
    └──────────────────────────────────────────────────────┘
    ```

## 2. Add a Layout Grid

  - Select the Desktop — 1440 frame itself.
  - In the right sidebar, find: `Layout grid`
  - Click the `+` button.
    
    > Figma will initially give you a basic grid. Click the grid settings/icon next to it.

  - Change the grid type from: `Grid` to: `Columns`

## 3. Configure your first 12-column grid

  - Start with these values—not because they're "perfect," but because they're easy to experiment with:

    |Category|Value / Type|
    |--------|------------|
    |Type|Stretch|
    |Count|12|
    |Margin|80|
    |Gutter|24|

    You'll get something roughly like:

    ```

        80px                                      80px
          ↓                                          ↓
    ┌─────┬────┐  ┌────┐  ┌────┐       ┌────┐  ┌────┬─────┐
    │     │    │  │    │  │    │       │    │  │    │     │
    │     │ C1 │  │ C2 │  │ C3 │  ...  │C11 │  │C12 │     │
    │     │    │  │    │  │    │       │    │  │    │     │
    └─────┴────┘  └────┘  └────┘       └────┘  └────┴─────┘
    Margin       ↑
                24px gutter
    ```

    ### Terminologies:

    - **Columns** - vertical areas where content can be placed. 
    - **Gutters** - spaces between columns. 
    - **Margins** - spaces between the outer columns and the edges of your frame.

## 4. Now actually use the grid

  - Don't stop after creating it. 
  - **Mini Challange**: Create some rectangles with `R`. Try making a sidebar that occupies approximately 3 columns:

    ```
    ┌───────────────┬─────────────────────────────────────┐
    │               │                                     │
    │    Sidebar    │                                     │
    │   3 columns   │          Main Content               │
    │               │          9 columns                  │
    │               │                                     │
    └───────────────┴─────────────────────────────────────┘
    ```

  - Then try cards in your main content:

    ```
    ┌───────────────┬────────────┬────────────┬────────────┐
    │               │            │            │            │
    │               │   Card 1   │   Card 2   │   Card 3   │
    │    Sidebar    │            │            │            │
    │               ├────────────┼────────────┼────────────┤
    │               │   Card 4   │   Card 5   │   Card 6   │
    │               │            │            │            │
    └───────────────┴────────────┴────────────┴────────────┘
    ```

  - Snap the edges of your rectangles to the column boundaries. This is where the purpose of the grid starts becoming obvious.

## 5. Experiment with the margin

  - Now change only: `Margin: 80` to: `Margin: 160`
  - Observe the columns. The content area becomes narrower because you're reserving more space on both sides.
  - Then try: `Margin: 32`. The content area becomes wider.
  - Think about the consequence:

    ```
    Small margins
    ←──────────────────────────────→
    More screen width available for content
    ```

    ```
    Large margins
            ←────────────────→
    Less screen width available for content
    ```

  - **Ask yourself:**
    - *Does my content feel too close to the edges?*
    - *Does it feel unnecessarily compressed?*

    > That's more important than memorizing 80px.

## 6. Experiment with the gutter

  - Return the margin to 80, then change: `Gutter: 24` to `Gutter: 8`
    > Your columns become visually closer together.

  - Then try: `Gutter: 48`. Now there's much more separation.
  - This affects things like cards:

    ```
    Small gutter:
    [ Card ][ Card ][ Card ]

    Large gutter:
    [ Card ]    [ Card ]    [ Card ]
    ```
  - **Gutters** control the separation between content regions.

## 7. Experiment with column count

  - Now change: `Count: 12` to `Count: 4`
  - You'll get a much simpler structure:

    ```
    |    1    |    2    |    3    |    4    |
    ```

  - Try: `Count: 6` and then return to `Count: 12`
  - A 12-column grid is popular because 12 divides nicely:

    ```
    12 ÷ 2 = 6
    12 ÷ 3 = 4
    12 ÷ 4 = 3
    12 ÷ 6 = 2
    ```

  - So the same grid can support many arrangements:

    ```
    2-column layout
    |------ 6 ------|------ 6 ------|

    3-column layout
    |--- 4 ---|--- 4 ---|--- 4 ---|

    4-column layout
    |-- 3 --|-- 3 --|-- 3 --|-- 3 --|

    Sidebar + content
    |-- 3 --|--------- 9 ---------|
    ```

    > That's one major reason 12-column grids are so common.

## Expected Outcomes

A grid gives unrelated elements shared alignment points.

Without a grid, you might accidentally create:

```

   Heading
        Card
     Image
             Button
```

With a grid, elements begin sharing boundaries:

```
│ Heading
│
│ ┌─────────┐  ┌─────────┐
│ │ Card    │  │ Card    │
│ └─────────┘  └─────────┘
│
│ Image
│
│ Button
↑
shared alignment
```

That's the main thing you should observe during this exercise: **columns aren't decoration**—they give your interface an underlying structure.
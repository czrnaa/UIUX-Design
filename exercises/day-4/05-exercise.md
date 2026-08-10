# Exercise 5

### Primary vs Secondary

1. Take your Button component.
2. Duplicate it.
    
    - Make one button:

      ```
      [ Continue ]
      ```

      Blue background
      White text

    - Make another:

    ```
    [ Cancel ]
    ```

    Transparent/neutral background
    Border
    Dark text

3. Select both components.

    Use:

    - Combine as variants
    - Figma creates a component set.

    You'll see something conceptually like:

    ```
    ┌──── Button ────────────────┐
    │                            │
    │ ◆ [ Continue ]             │
    │                            │
    │ ◆ [ Cancel ]               │
    │                            │
    └────────────────────────────┘
    ```

4. Look at the properties Figma created.
    - It may initially give you something generic such as:
    
    ```
    Property 1
    ```
    
    - Rename it: `Type`
    - Then rename the values:
    
    ```
    Primary
    Secondary
    ```

5. Your component system now means:

```
Button
│
└── Type
    ├── Primary
    └── Secondary
```

6. Now test it
    - Drag an instance of Button onto your Playground.
    - Select it.
    - In the right sidebar, you should be able to change:
    ```
    Type

    Primary ▼
    ```

    to:

    ```
    Type

    Secondary ▼
    ```

And... Observe what happens. 

## Expected Input
- You didn't replace the component.
- You changed its variant property.
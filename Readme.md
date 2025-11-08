## New Features

Two new blocks have been added to the "Operators" category:

1.  **`square [ ]`**: Calculates the square of a number (number * number).
2.  **`square root of [ ]`**: Calculates the square root of a number.

## Code Changes

### 1. `scratch-blocks` Repository

This repository contains the visual definitions of the blocks.

-   **`scratch-blocks/blocks_vertical/operators.js`**
    -   Added the block definitions for `operator_square` and `operator_squareroot`. This defines the block's appearance, inputs, and category.

-   **`scratch-blocks/msg/messages.js`** & **`scratch-blocks/msg/json/en.json`**
    -   Added localization keys and English translations (`OPERATORS_SQUARE` and `OPERATORS_SQUAREROOT`) for the new block labels.

### 2. `scratch-vm` Repository

The Vm repository is where the logic for the blocks is executed.

-   **`scratch-vm/src/blocks/scratch3_operators.js`**
    -   Added the implementation logic for the `square` and `squareroot` primitives.
    -   The `square` function computes the product of the input number with itself.
    -   The `squareroot` function computes the square root of the input number using `Math.sqrt()`.

### 3. `scratch-gui` Repository

This repository handles the user interface(GUI), including the block toolbox.

-   **`scratch-gui/src/lib/make-toolbox-xml.js`**
    -   Added the XML definitions for `operator_square` and `operator_squareroot` to the `operators` category.
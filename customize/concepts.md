---
layout: default
parent: Customize
nav_order: 2
---
# Concepts

What makes MoonHare  **customizable**

MoonHare is highly customizable thanks to  **Sass variables** .

These variables exist at 4 levels:

-   **[initial variables]()**: global variables with  **literal**  values
-   **[derived variables]()**: global variables with values that reference other variables, or are computed
-   **[generic variables]()**: for the HTML elements which carry no CSS class
-   **element/component variables**: variables that are specific to a Bulma element/component

Since these variables carry the  `!default`  flag, they can be assigned a  **new value**  either before or after having been imported.

### Strategy

To customize MoonHare, you will need to:

-   **install**  (or download) MoonHare
-   have a working  **Sass setup**
-   create your own  `.scss`  or  `.sass`  file

This can be achieved with any of the following:

-   [node-sass]()
-   the  [Sass CLI]()
-   [webpack]()

# dcim-scripts
Collection of scripts in dc:im, my stack machine language.

These are definitely not written optimally for the latest language version, but should still work.
## Minimized versions
The `min` directory contains functionally identical versions of scripts with all comments and unnecessary whitespace removed.
## List of scripts
- `autoprint.dcim`: Enters a prompt loop (like interactive mode) and prints the whole stack after every action. Exit and cleanup: `2QL?1C`.
- `bintree.dcim`: Prompts for a number, generates and prints a "binary tree" pattern of that degree. Also known as the "ruler function" or the optimal solution for a Tower of Hanoi puzzle.
  - Degree 4 example: `1 2 1 3 1 2 1 4 1 2 1 3 1 2 1`
- `calendar.dcim`: Prints the calendar of a given year.
  - Gregorian calendar, only correct after 1582 CE.
- `approx.dcim`: Approximates any positive number as a rational. Generates successively better approximations until exact equality is reached. The "error reduction factor" (1 if omitted) dictates how many times closer a new approximation needs to be before it is accepted. Higher values make it converge faster, but also increase the chance of missing a useful approximation you want.

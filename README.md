# dcim-scripts
Collection of scripts in dcim, my stack machine language
## Safety guidelines
To not mess up the existing working environment when executed using `&`, "safe" scripts should:
- Preserve the environment parameters:
  - Start with `{` and end with `}`.
  - Manually save and restore the working precision if changing it is necessary.
- Not affect the pre-existing contents of the stack and registers:
  - Be careful with the stack, use `C` instead of `c` or temporarily move it to a register.
  - *Push* macros to registers (`SR` instead of `sR`).
  - Clean up registers after finishing (`LR` and `C`).
- Document their expected inputs and outputs.
- Document all behaviour that doesn't meet the above guidelines.
## Minimized versions
The `min` directory contains functionally identical versions of scripts with all comments and unnecessary whitespace removed.
## List of scripts
- `autoprint.dcim`: Enters a prompt loop (like interactive mode) and prints the whole stack after every action. Exit and cleanup: `2QL?1C`.
- `brainfuck.dcim`: Brainfuck interpreter. `[` and `]` are replaced with `(` and `)`.
- `bintree.dcim`: Prompts for a number, generates and prints a "binary tree" pattern of that degree. Unsafe, intended for one-off usage.
  - Degree 4 example: `1 2 1 3 1 2 1 4 1 2 1 3 1 2 1`

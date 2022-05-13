# dcim-scripts
Collection of scripts in dcim, my stack machine language
## Safety guidelines
To not mess up the existing working environment when executed using `&`, "safe" scripts should:
- Preserve the environment parameters:
  - Start with `{` and end with `}`.
  - Manually save and restore the working precision if changing it is necessary.
- Not affect the pre-existing contents of the stack and registers:
  - *Push* macros to registers (`SR` instead of `sR`).
  - Clean up registers after finishing (`LR` and `C`).
- Document their expected inputs and outputs.
- Document all behaviour that doesn't meet the above guidelines.

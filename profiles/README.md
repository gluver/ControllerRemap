# AntiMicroX Profiles

## Codex Vibe Coding

Load `codex-vibe-coding.amgp` in AntiMicroX while the controller is in Xbox Wireless Controller mode.

| Physical control | AntiMicroX action |
| --- | --- |
| A | Ctrl+Shift+D |
| B | Win+H |
| X | Esc |
| Y | Enter |
| ZR | PageDown |
| ZL | Mouse button 4 |
| Home | Mouse button 5 |
| Extra button 11 | PageUp |
| D-pad Up | Up |
| D-pad Down | Down |
| D-pad Left | Left |
| D-pad Right | Right |
| - | Ctrl+Z |
| + | Ctrl+Enter |

Notes:

- This profile is calibrated from AntiMicroX's observed button indices for this controller. Those indices do not line up cleanly with the browser Gamepad API probe, so the `.amgp` file is the source of truth for AntiMicroX behavior.
- `Capture` is not mapped because it did not produce a Gamepad API event in Xbox mode.
- If `Ctrl+C`, `Ctrl+V`, `Ctrl+Z`, or `Ctrl+Enter` do not trigger correctly, create one combined-key assignment in the AntiMicroX UI, save it, and compare the generated XML against this profile.

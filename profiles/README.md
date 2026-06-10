# AntiMicroX Profiles

## Codex Vibe Coding

Load `codex-vibe-coding.amgp` in AntiMicroX while the controller is in Xbox Wireless Controller mode.

| Physical control | AntiMicroX action |
| --- | --- |
| A | Ctrl+Shift+D |
| B | Win+H |
| X | Esc |
| Y | Enter |
| L | Shift+Tab |
| R | Tab |
| ZL | PageUp |
| ZR | PageDown |
| D-pad Up | Up |
| D-pad Down | Down |
| D-pad Left | Left |
| D-pad Right | Right |
| - | Ctrl+Z |
| + | Ctrl+Enter |

Notes:

- Browser Gamepad API button numbers are zero-based. AntiMicroX profile button indices are one-based, so browser `Button 0` is written as AntiMicroX `<button index="1">`.
- `Capture` is not mapped because it did not produce a Gamepad API event in Xbox mode.
- If `Ctrl+C`, `Ctrl+V`, `Ctrl+Z`, or `Ctrl+Enter` do not trigger correctly, create one combined-key assignment in the AntiMicroX UI, save it, and compare the generated XML against this profile.

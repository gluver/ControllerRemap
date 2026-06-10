# ControllerRemap

A small Windows-focused workspace for testing a Bluetooth controller and using it for Codex vibe coding.

The project currently contains:

- `index.html`: a local browser probe for reading raw Gamepad API and keyboard events.
- `profiles/codex-vibe-coding.amgp`: an AntiMicroX profile for Xbox Wireless Controller mode.
- `profiles/README.md`: the profile keymap.

## Codex Vibe Coding Profile

Load `profiles/codex-vibe-coding.amgp` in AntiMicroX while the controller is connected in Xbox Wireless Controller mode.

Current A/B/X/Y mapping:

| Controller key | Action | Purpose |
| --- | --- | --- |
| A | `Ctrl+Shift+D` | Codex Dictate |
| B | `Win+H` | Windows system dictation |
| X | `Esc` | Cancel / No |
| Y | `Enter` | Confirm / Yes |

Other useful mappings:

| Controller key | Action |
| --- | --- |
| L | `Shift+Tab` |
| R | `Tab` |
| ZL | `PageUp` |
| ZR | `PageDown` |
| D-pad | Arrow keys |
| - | `Ctrl+Z` |
| + | `Ctrl+Enter` |

Note: this controller reports `+/-` differently in AntiMicroX than in the browser Gamepad API probe. The profile has been adjusted to the AntiMicroX-observed behavior: physical `-` maps through profile button index `5`, and physical `+` maps through profile button index `7`.

## Load the AntiMicroX Profile

1. Install and open AntiMicroX.
2. Connect the controller in Xbox Wireless Controller mode.
3. In AntiMicroX, choose `Load` or `Open Profile`.
4. Select `profiles/codex-vibe-coding.amgp`.
5. Test the profile in Codex, Notepad, or another text input.

If combined shortcuts such as `Ctrl+Shift+D`, `Win+H`, or `Ctrl+Enter` do not trigger correctly, create one combined-key assignment in the AntiMicroX UI, save it as a new profile, and compare the generated XML with `profiles/codex-vibe-coding.amgp`.

## Input Probe

Open `index.html` directly in a browser to inspect raw input.

1. Click `Focus page`.
2. Put the controller in Xbox Wireless Controller mode.
3. Press any controller button once. Browsers often expose the gamepad only after the first press.
4. Record which button indices and axis values change.
5. Optional: switch the controller to keyboard mode and watch the keyboard event log.

Observed Xbox mode mapping for this controller:

| Controller key | Raw input |
| --- | --- |
| A | `Button 1` |
| B | `Button 0` |
| X | `Button 3` |
| Y | `Button 2` |
| L | `Button 4` |
| R | `Button 5` |
| ZL | `Axis 2`, released `-1.000`, pressed `1.000` |
| ZR | `Axis 5`, released `-1.000`, pressed `1.000` |
| - | `Button 6` |
| + | `Button 7` |
| Home | `Button 10` |
| Capture | No observed response |
| D-pad up | `Axis 9 = -1.000` |
| D-pad right | `Axis 9 = -0.429` |
| D-pad down | `Axis 9 = 0.143` |
| D-pad left | `Axis 9 = 0.714` |
| D-pad released | `Axis 9 = 1227133568.000` |

The D-pad release value is an abnormal sentinel value from this controller/driver combination. Treat values above `1` as released.

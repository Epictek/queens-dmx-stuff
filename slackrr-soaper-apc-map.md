# Slackrr / SOAPER — APC mini mk2

Grid rows run top to bottom. All mappings use Universe 3 (internal ID 2). Use standard clip mode.

Colour/look pad LEDs match their look: pink, cyan, blue, purple, red, amber or white. Split looks and swaps use pink for Slackrr and amber for SOAPER; multicolour party/chill/punk looks use magenta. Pads stay steady when idle and pulse when active. These feedback colours are saved in the workspace (APC palette: white 3, red 5, amber/orange 9, cyan 37, blue 45, purple 49, magenta 53, pink 57).

| Row | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | HOUSE | CHANGEOVER | MC / HOST | ACOUSTIC | COLOUR CHILL | PARTY | Spare | STOP ALL |
| 2 | SLACKRR PINK / CYAN | SLACKRR CHORUS | SLACKRR BRIDGE | SOAPER BLUE VERSE | SOAPER AMBER / BLUE | SLACKRR CHASE | SLACKRR SWAP | ENCORE |
| 3 | PINK | CYAN | BLUE | PURPLE | RED | AMBER | SLACKRR SPLIT | SOAPER SPLIT |
| 4 | WHITE | SLACKRR SWAP | SOAPER SWAP | PUNK COLOURS | ROCK | OCEAN | PURPLE HAZE | SUNSET |
| 5 | SLOW CIRCLE | SWEEP | PARTY CIRCLE | CROWD SWEEP | CEILING CIRCLE | RELATIVE CIRCLE | WALKOUT | MOVEMENT TIME RESET MULTIPLIER |
| 6 | FRONT SPOT | WIDE BAND | BACKLINE | CROWD | COLOUR CHASE | PAR FADE | STROBE | FX TEMPO RESET MULTIPLIER |
| 7 | OPEN | GOBO 1 | GOBO 2 | GOBO 3 | GOBO 4 | GOBO 5 | GOBO 6 | Spare |
| 8 | SWEEP STAGE | STAGE CENTRE | Spare | Spare | Spare | Spare | Spare | Spare |

## Buttons directly above faders

| Button (left to right) | Function | MIDI note |
| --- | --- | --- |
| 1 | PARS FLASH [hold] | 100 |
| 2 | BLINDER [hold] | 101 |
| 3 | LOOK FADE SLOWER / LONGER | 102 |
| 4 | LOOK FADE FASTER / SHORTER | 103 |
| 5 | BACK WASH FLASH [hold] | 104 |
| 6 | WHITE OUT [hold] | 105 |
| 7 | Spare | 106 |
| 8 | Spare | 107 |

## Right-side buttons

| Button (top down) | Function |
| --- | --- |
| 1 | FX TEMPO TAP |
| 2 | FX TEMPO SLOWER / LONGER |
| 3 | FX TEMPO FASTER / SHORTER |
| 4 | MOVEMENT TIME TAP |
| 5 | MOVEMENT TIME SLOWER / LONGER |
| 6 | MOVEMENT TIME FASTER / SHORTER |
| 7 | LOOK FADE TAP |
| 8 | LOOK FADE RESET MULTIPLIER |

## Faders

| Fader | Function | CC |
| --- | --- | --- |
| 1 | PARS | 48 |
| 2 | MOVERS | 49 |
| 3 | Unassigned | 50 |
| 4 | Unassigned | 51 |
| 5 | BACK WASH | 52 |
| 6 | Unassigned | 53 |
| 7 | GENERIC RGB | 54 |
| 8 | STROBE | 55 |
| 9 | MASTER | 56 |

BACK WASH FLASH raises only rear dimmers to DMX 35, preserving current colours. Select a rear colour first. The back-wash slider also tops out at 35. White Out remains an explicit white hit.
All flash buttons are momentary: hold to flash, release to stop. FX reset is now grid row 6 column 8; movement reset is grid row 5 column 8.
Use the bundled APC profile and select the APC input and feedback port on Universe 3. STOP ALL stops functions, while MASTER down gives complete blackout. Manual focus pages are on-screen controls.
Mappings validated offline; physical input and feedback require checking.

SWEEP STAGE (grid row 8, column 1) first targets the calibrated STAGE CENTRE positions, then pans ±12 DMX around them with tilt held fixed. MOVEMENT TIME controls the four-leg cycle. Calibrated centre pan: movers 0/3 = 134, movers 1/2 = 45; all tilts = 57. Colours/intensity come from your active look. Toggle off to release movement.

STAGE CENTRE: POSITION bank, APC row 8 column 2. Position-only scene for movers 0–3, calibrated to stage centre. SWEEP STAGE uses matching centre positions and ±12 pan endpoints; future focus changes require updating the sweep endpoints too.

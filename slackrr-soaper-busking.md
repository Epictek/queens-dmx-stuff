# Slackrr + SOAPER — busking

Open `slackrr-soaper-busking.qxw` in QLC+ 5.2.2. Based on the current `january-jam.qxw`.

## Rear patch

Four **additional** UKING ZQ01638 fixtures, Standard mode (8 channels), on Universe 1. Left/right is viewed from the audience.

| Fixture | DMX start | Last channel |
| --- | ---: | ---: |
| Back wash 1 — left | 408 | 415 |
| Back wash 2 — mid left | 416 | 423 |
| Back wash 3 — mid right | 424 | 431 |
| Back wash 4 — right | 432 | 439 |

The original ZQ01638 remains at 400–407. ArtNet output length is now 439 channels. Existing ArtNet destination and MIDI device mappings are inherited.

Profile order: dimmer, red, green, blue, white, strobe, function, effects/fade. The profile must be installed on the playback computer (`UKING-ZQ01638.qxf`).

## Playing the show

The four rear-wash dimmers are limited directly to **DMX 35** in all existing scenes (including BACK WASH FLASH and WHITE OUT). The BACK WASH slider maps its full travel to 0–35. The earlier output modifier is no longer attached, so there is no double-scaling or modifier installation requirement. This limits the programmed controls; newly created scenes or manual DMX controls must also respect 35.

1. Raise MASTER, choose a position and a LOOK, then raise **BACK WASH x5**. Rear colours are separate from dimmer level; the back-wash fader starts at zero.
2. **SOAPER:** blue verse and amber/blue split. **Slackrr:** pink/cyan split, chorus pink and purple bridge. These are creative palettes for this workspace, not supplied band branding.
3. The right-hand **REAR COLOURS** and **REAR CHASES** banks control only the four new fixtures. Colours are mutually exclusive within their bank, and chases within theirs; starting a chase no longer switches off the selected base colour. Click the active chase again to release it. Both banks write rear colour channels, so their output can interact while both are active. Main LOOKS and their chase steps do not write any rear-wash channels, leaving rear colour and intensity independent. WHITE OUT remains an explicit momentary white override.
4. **SPEED** controls the new rear chases alongside the existing colour/strobe chases. **DURATION** controls the existing movement bank. The new rear chases alternate colours, leaving intensity on the back-wash fader.
5. **BACK WASH FLASH** raises only the four rear dimmers to 35, preserving the selected colours; select a rear colour first. All flash controls use APC buttons directly above the faders: **1 PARS FLASH, 2 BLINDER, 5 BACK WASH FLASH, 6 WHITE OUT**. Their on-screen buttons are above the corresponding sliders too. **WHITE OUT** remains a white hit (rear dimmer 35) plus the original front/mover white look. FX and movement multiplier resets moved to grid row 6 column 8 and row 5 column 8 respectively.
6. **STOP ALL** stops functions; direct level faders can still output. Use **MASTER at zero** for a complete blackout. Level faders are direct HTP levels, not subtractive group masters.

All 56 performance buttons, six faders and three timing controls are mapped to the APC mini mk2 on Universe 3. Individual PAR RGB sliders have been removed from both performance and setup pages; APC faders 3, 4 and 6 are unassigned. The back-wash fader remains CC 52 and covers the four rear ZQ01638s. See `slackrr-soaper-apc-map.html` for the controller chart and `slackrr-soaper-apc-map.md` for MIDI details and setup. The bundled `slackrr-soaper-apc-mini-mk2.qxi` profile is required. The old mixed APC/encoder mappings have been replaced with unique APC assignments.

Existing mover positions are inherited venue focuses: check them during focus. The two 19PCS moving washes and Generic RGB fixture retain their original patch/controls.

## Validation

Checked XML parsing, all 14 fixture patches for overlap and universe bounds, scene channel/value ranges, chaser references, button targets, fader channels and speed-dial references. Live QLC+ playback and physical fixtures have not been tested here.

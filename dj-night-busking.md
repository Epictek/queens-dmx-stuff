# DJ Night — multi-genre busking

Open `dj-night-busking.qxw` in QLC+ 5.3.0. New workspace derived from `slackrr-soaper-busking.qxw`; same ArtNet output, APC mini mk2 input and fixture addresses for everything carried over.

## Rig and patch (Universe 1, ArtNet 439ch)

| Fixture | QLC+ ID | DMX start | Channels |
| --- | ---: | ---: | ---: |
| LED Spot 100W movers (LEFT/RIGHT FRONT, RIGHT/LEFT BACK) | 0–3 | 1 / 19 / 28 / 10 | 9 |
| Generic RGB | 6 | 228 | 4 |
| **19PCS STACK LEFT** (above left speaker stack, front of stage) | 9 | 77 | 16 |
| **19PCS STACK RIGHT** (above right speaker stack) | 8 | 101 | 16 |
| **PAR LEFT 1–5** (front/house washes, Par 36, individually controlled) | 12–16 | 168 / 175 / 182 / 189 / 196 | 7 |
| **PAR RIGHT 1–2** (front/house wash) | 17–18 | 203 / 210 | 7 |
| **BACK WASH 1–4** (UKING ZQ01638 back-stage washers: LEFT / MID LEFT / MID RIGHT / RIGHT) | 19–22 | 408 / 416 / 424 / 432 | 8 |

The seven Par 36s (5 left, 2 right, audience perspective) are the **front / house washes**. The four ZQ01638s are the **back-stage washers**, on the same 408–439 patch as the band workspace — their dimmers are capped at DMX 35 (carried over from the band setup; raise the cap in the BACK WASH fader's high limit and the REAR scenes if you want more). The two 19PCS moving-head washes sit above the speaker stacks in front of the stage — full pan/tilt, RGBW, zoom and shutter. Fixture groups: MOVING HEADS, PARS - LEFT TO RIGHT (7×1: L1–L5, R1, R2), STACK MOVERS (ID 9 left, ID 8 right), BACK WASH - LEFT TO RIGHT (4×1).

## Playing the night

1. MASTER up, pick a genre look (LOOKS bank), a position (POSITION bank), raise PARS and STACKS faders.
2. Genre looks: HOUSE, DNB, GARAGE, TECHNO, DISCO, HIP HOP, CHILL, PARTY (on-screen only), plus WALK-IN and MC / HOST. Each sets all 7 front pars (left/right splits where it matters), stack movers' colour/dimmer and spot-mover colour/gobo/dimmer. Back-stage washes stay independent of genre looks.
3. PAR COLOURS set colour only on the seven front pars; intensity stays on the PARS fader. PAR FX are RGB matrices across the 7-par group: RUN (stripe chase), ONE BY ONE, EVEN/ODD, STROBE.
4. STACKS bank: seven colours plus SWAP and CHASE for the 19PCS pair (colour + shutter open; dimmer on the STACKS fader). Stack movement: STACK CIRCLE (APC row 7 pad 8) and STACK SWEEP (on-screen), both under MOVEMENT TIME.
5. BACK-STAGE WASHES: the REAR COLOURS frame (bottom of middle column) has seven colours plus REAR SWAP (left-pair / right-pair alternation) and REAR CHASE — colour only, both beat-synced under FX TEMPO. Intensity is the BACK WASH fader (APC fader 3, capped at 35), momentary REAR FLASH is the middle flash button.
6. Individual front-par control: APC bottom row (pads 1–7) flashes L1–L5, R1, R2 white; on-screen the PARS - INDIVIDUAL FLASH frame does the same, and Page 2 has per-par DIM/R/G/B sliders plus mover/stack XY pads and stack DIM/RGBW sliders.
7. Flash row above the faders: PARS FLASH (dimmer), BLINDER, PARS WHITE, STK FLASH, REAR FLASH, WHITE OUT — all momentary. The STROBE fader covers movers, all 7 front pars, the 19PCS shutter and the back washers' strobe channel (bottom of travel = open, push up for strobe / random / thunder).
8. Dials: FX TEMPO (front-par colour chase, strobes, stack swap/chase, rear swap/chase, all PAR FX matrices), MOVEMENT TIME (all mover + stack EFX and SWEEP STAGE), LOOK FADE (genre/utility looks). APC side buttons: tap/reset as before — see `dj-night-apc-map.md`.
9. STOP ALL stops functions; faders are direct HTP levels, so MASTER down for full blackout (BLACKOUT also drops the rear washers).

## Audio-reactive automation (FFT from the mixer)

The workspace is set up for a line-level feed from the mixer into the laptop (audio interface or line-in):

1. In QLC+ → Inputs/Outputs → Audio, pick the capture device the mixer is plugged into. The device choice is a global QLC+ setting, not saved in the workspace, so set it once on the playback laptop.
2. The workspace's beat generator is set to **Audio**: QLC+'s built-in FFT beat tracker (spectral flux on the low band, adaptive threshold) follows the music live. 120 BPM is just the fallback.
3. Beat-synced chases (`<Tempo>Beats</Tempo>`, 1 beat per step): **PAR COLOUR CHASE, STK SWAP, STK CHASE, REAR SWAP, REAR CHASE**. They lock to the track automatically; the FX TEMPO dial still works as a multiplier on top.
4. An **Audio Triggers** widget on Page 2 (8 spectrum bars across 0–5000 Hz, 625 Hz each) drives energy automation:
   - Bar 1 (0–625 Hz, kick/bass) → taps **FX TEMPO** on every hit
   - Bar 3 (1250–1875 Hz, snare) → taps **MOVEMENT TIME** every 2nd hit
   - Bar 5 (2500–3125 Hz, presence) → starts **PARTY CIRCLE** while the mix is busy (on ≥80%, off <50%)
   - Bar 8 (4375–5000 Hz, air) → **PAR STROBE** on the brightest peaks only (on ≥92%, off <80%)

Tune the thresholds live: double-click the widget in design mode. If the kick bar double-fires on bass-heavy genres, raise its enable threshold a few points; if the strobe never fires, drop bar 8's threshold. The volume bar is unassigned — just a meter.

## Validation

Generated programmatically. Checked: XML parses, no DMX overlap within the 439-channel ArtNet range, all chaser steps / button targets / dial functions resolve, scene channel/value ranges within fixture widths, unique VC widget IDs, unique APC input channels, audio-trigger bar references resolve to existing widgets/functions. Not yet tested against live QLC+ playback or physical fixtures — verify mover colour-wheel values, stack-mover pan/tilt orientation, focus positions, back-washer address switches (408/416/424/432), and beat-tracking against real mixer audio during soundcheck.

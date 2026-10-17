# DJ Night — APC mini mk2

Grid rows run top to bottom. All mappings use Universe 3 (internal ID 2). Same profile as the band workspace (`slackrr-soaper-apc-mini-mk2.qxi`, "Akai APC Mini mk2 - Slackrr SOAPER") — no new profile to install. Pads steady when idle, pulsing when active. LED palette: white 3, red 5, amber 9, yellow 13, green 21, cyan 37, blue 45, purple 49, magenta 53, pink 57.

| Row | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | WALK-IN | MC / HOST | HOUSE | DNB | GARAGE | TECHNO | DISCO | STOP ALL |
| 2 | HIP HOP | CHILL | STK PINK | STK CYAN | STK BLUE | STK PURPLE | STK RED | STK AMBER |
| 3 | PAR RED | PAR ORANGE | PAR YELLOW | PAR GREEN | PAR CYAN | PAR BLUE | PAR PURPLE | PAR MAGENTA |
| 4 | PAR WHITE | PAR RUN | PAR ONE BY ONE | PAR EVEN/ODD | PAR STROBE | STK WHITE | STK SWAP | STK CHASE |
| 5 | SLOW CIRCLE | SWEEP | PARTY CIRCLE | CROWD SWEEP | CEILING CIRCLE | RELATIVE CIRCLE | SWEEP STAGE | MOVEMENT TIME RESET |
| 6 | FRONT SPOT | WIDE BAND | BACKLINE | CROWD | COLOUR CHASE | PAR FADE | STROBE | FX TEMPO RESET |
| 7 | OPEN | GOBO 1 | GOBO 2 | GOBO 3 | GOBO 4 | GOBO 5 | GOBO 6 | STACK CIRCLE |
| 8 | PAR L1 FLASH | PAR L2 FLASH | PAR L3 FLASH | PAR L4 FLASH | PAR L5 FLASH | PAR R1 FLASH | PAR R2 FLASH | STAGE CENTRE |

PARTY, STACK SWEEP and the REAR colour bank (7 colours + REAR SWAP / REAR CHASE) exist on screen only (no free pads) — see the REAR COLOURS frame on page 1.

## Buttons directly above faders

| Button (left to right) | Function | MIDI note |
| --- | --- | --- |
| 1 | PARS FLASH (dimmer, all 7 front pars) [hold] | 100 |
| 2 | BLINDER [hold] | 101 |
| 3 | PARS WHITE (white, all 7 front pars) [hold] | 102 |
| 4 | STK FLASH [hold] | 103 |
| 5 | REAR FLASH (back-stage washers) [hold] | 104 |
| 6 | WHITE OUT [hold] | 105 |
| 7 | Spare | 106 |
| 8 | Spare | 107 |

## Right-side buttons

| Button (top down) | Function |
| --- | --- |
| 1 | FX TEMPO TAP |
| 2 | Spare |
| 3 | Spare |
| 4 | MOVEMENT TIME TAP |
| 5 | Spare |
| 6 | Spare |
| 7 | LOOK FADE TAP |
| 8 | LOOK FADE RESET |

FX TEMPO RESET is grid row 6 column 8; MOVEMENT TIME RESET is grid row 5 column 8.

## Faders

| Fader | Function | CC |
| --- | --- | --- |
| 1 | PARS (all 7 front pars) | 48 |
| 2 | MOVERS | 49 |
| 3 | BACK WASH (4 rear washers, capped at 35) | 50 |
| 4 | STACKS (19PCS dimmer) | 51 |
| 5 | GENERIC RGB | 52 |
| 6 | STROBE (movers, all 7 front pars, 19PCS shutter, back washers) | 53 |
| 7 | Spare | 54 |
| 8 | Spare | 55 |
| 9 | MASTER | 56 |

STK FLASH raises both stack-mover dimmers to full with the shutter open, preserving the selected colour — pick a stack colour first. The STROBE fader's bottom of travel is open (no strobe); push up for strobe, random strobe, then thunder on the 19PCS. Par colour and stack colour pads write colour channels only; intensity lives on the faders. Bottom-row par flash pads are momentary white per individual front par (L1–L5, R1, R2). STOP ALL stops functions; MASTER down for complete blackout. Page 2 of the VC holds per-par DIM/R/G/B sliders, spot-mover and 19PCS XY pads, stack DIM/RGBW sliders, and the Audio Triggers spectrum widget.

Audio: with a mixer feed on the audio input, PAR COLOUR CHASE / STK SWAP / STK CHASE / REAR SWAP / REAR CHASE run beat-synced (1 beat per step), kick hits tap FX TEMPO, snare hits tap MOVEMENT TIME, the presence band brings in PARTY CIRCLE, and the air band fires PAR STROBE on big peaks. See `dj-night-busking.md`.

Mappings validated offline; physical input and feedback require checking on the night.

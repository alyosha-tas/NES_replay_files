# NES-replay-files

These files sync using the TAStm32 replay device on a front loading NES from power on.
Unless otherwise noted below, use --blank 1

Additionally, the following runs require RAM cleared to the pattern used by default in FCEUX / BizHawk: Adventures of Tom Sawyer, Marble Madness, Mickey Mousecapade, Monopoly (both runs), Rad Racer, Silver Surfer, Wizards and Warriors (both runs.) Some games that require RAM clearing require a start from reset as RAM is too volatile, for these cases use --blank 0.

Metroid low percent requires the following command:
py -3 python\tastm32.py --console nes --players 1,5 --blank 0 --dpcm metroid_frame.r08

Karate Champ may require blank 3 instead of 1 due to uninitialized RAM.

Solar Jetman starts from a reset  so should use --blank 0. However the run still syncs from power on, it just doesn't skip the intro copyright screen.

Quattro Adventure runs use a reset that is performed manually. An extra input is added to the .r08 after the rest to account for this, as the bot recognizes it as an extra input. It may be that not all bots require this.

# TRX Workout Timer

Single-file browser timer for a TRX / Tabata-style workout. It was moved into this project from the Codex thread `019f1cf3-03ce-75a0-b3a9-64d4ee1d910a`.

## Deliverable

- Main file: `index.html`
- Logo asset: `assets/trx-timer-logo.png`
- Original source file copied from: `/Users/giorgioiezzi/Documents/Codex/2026-07-01/okay-so-i-need-you-to/outputs/trx-tabata-timer.html`
- No build step or app install is required. The page is designed to open directly in a browser.

## Default Workout

- Timer name: `TRX workout`
- Sets: `10`
- Reps per set: `6`
- Rep duration: `24` seconds
- Rest between reps: `10` seconds
- Rest between sets: `15` seconds
- After rep 6, the 15-second set rest replaces the normal 10-second rep rest.
- Total default duration: `34:35`

Total math:

- Work: `10 * 6 * 24s = 24:00`
- Between-rep rests: `10 sets * 5 rests * 10s = 8:20`
- Between-set rests: `9 rests * 15s = 2:15`
- Total: `34:35`

## Current Features

- Start, Pause, and Reset playback controls.
- Automatic phase tracking for Work, Rep Rest, Set Rest, and Finished.
- Saved custom timers using browser `localStorage`.
- New, Copy, Delete, Save, and Revert timer editing flows.
- Editable timer name, sets, reps per set, rep seconds, rep rest seconds, and set rest seconds.
- Sound cues for transitions.
- Responsive desktop and mobile layout.
- Premium generated logo used for the header mark and favicon.
- Timer editor is hidden after saving or selecting a saved timer.
- Modify button reopens the editor; Hide closes it again.
- Skip control was removed per the latest browser comment.
- My Timers is collapsed by default and appears above the timer so saved timers are easy to reach without taking over the phone layout.
- Music is collapsed by default and offers No music or Italian radio.
- Italian radio includes 20 mainstream Italian stations with Previous Radio and Next Radio controls.
- Starting the workout starts the selected radio stream; pausing/resetting the timer pauses/stops radio.
- Music volume and Cue volume have large visible sliders.
- Cue sounds and spoken countdowns automatically lower the music volume temporarily, then restore it.
- While the timer runs, the app requests a screen wake lock where the browser supports it.

## Music Sources

- No music mode: starts the timer without loading any audio stream. Voice cues and beeps still work.
- Italian Radio mode: 20 mainstream stations, using direct audio or HLS streams verified to respond as browser-playable media.
  - RTL 102.5, Radio Italia, RDS, Radio Deejay, Radio 105, Radio Kiss Kiss
  - Rai Radio 1, Virgin Radio, Radio 24, Rai Radio 2, R101, Radio Monte Carlo
  - Radio Capital, m2o, Radiofreccia, Radio Zeta, Radio Bruno, Radio Subasio
  - Radio Norba, Radio Parsifal

## Old Thread Notes

The original request was to build a website or plain HTML file because the user wanted the user's mom to use it without downloading an app.

The first completed version was verified in the old thread with Playwright on desktop `1440x920` and mobile `390x844`. That pass checked start, pause, reset, the rep-6 transition into a 15-second Set Rest, custom timer save, reload persistence, delete confirmation, responsive layout, and console cleanliness after the favicon fix.

The latest follow-up edit in the old thread was interrupted after code patches had been applied. Those patches are present in this project copy: the editor starts collapsed with a Modify/Hide toggle, and the Skip button has been removed.

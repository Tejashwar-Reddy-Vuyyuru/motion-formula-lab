# Formula Play

Draw it. Say it. Get the formula.

Formula Play turns a drawing, a ringing sound or a short video of a moving object into a formula, and turns a formula back into a drawing or a sound. It runs entirely in the browser on a phone. There is no account and nothing is uploaded.

**Live app:** https://tejashwar-reddy-vuyyuru.github.io/motion-formula-lab/formula-play.html

## What it does

### Create
- **Draw.** Draw with a finger, up to eight lines in one picture. A plain shape gets its equation (line, parabola, wave or circle). Anything else becomes a sum of spinning circles that redraw it.
- **Type a formula.** Write `y = f(x)` or a pair `x(t)`, `y(t)` and watch it draw itself.
- **From a video.** Film or choose a clip of a pendulum, a dropped object or a thrown ball. Tap the object, confirm what the app followed, and get the formula of its motion with a replay, graphs and predictions.
- Extras: keep a drawing replaying (signature mode), morph one drawing into another, hear a line as a sound, and make a poster.

### Sound
- **Tuner.** The note, how far out of tune it is, how fast the sound fades, its overtones and its formula.
- **Tune.** Hum or whistle for 8 seconds and get the notes written down and played back.
- **Voice pen.** The pitch of your voice moves a pen up and down across the screen.
- **Chords.** Tap up to four notes; the app plays them and names the chord.

### Games
- **Today's challenge.** One formula a day: read it, draw what it looks like, get a score out of 100.
- **Practice** with five levels, **Name the curve**, a 60-second **Speed round**, and **duels** sent to a friend by link.

### Menu
Progress, saved creations, opening a formula code, help, settings (light or dark, motion effects, clear data) and about.

## Sending

Every creation can be sent as a link. The link holds the formula itself, so it opens straight to the drawing, formula, sound or tune. Where links cannot carry data, the same formula travels as a short text code starting with `FP1`.

## How it works

- **Drawings.** Each line is sampled evenly along its length and written as a Fourier series, which is a sum of rotating circles. Simple shapes are also fitted directly by least squares.
- **Sounds.** Pitch is found with the YIN method, overtones by projecting the signal onto multiples of the pitch, and the fade from the slope of loudness over time.
- **Video.** Frames are compared with a background picture to find what moved. The tapped object is followed by colour and by motion, and the simplest formula that fits held-out data is kept. If nothing fits, the app says so.
- **Typed formulas** are read symbol by symbol by a small parser. No code from the text is ever run.

## How it has been tested

Tested with automated browser runs at phone size:

- Drawn lines, parabolas, waves and circles come back with the right equation; free drawings are matched to 99% or better.
- Thirteen computer-made tones from 82 to 1760 Hz were read to within 0.4 hundredths of a note-step.
- Nine computer-made melodies were written down with every note right; noise was refused.
- Three real video clips (pendulum, thrown ball, dropped ball) gave the expected kind of formula through each route: confirm, pick a line, and mark by hand.

Not yet tested:

- Real instruments, real humming and real voices.
- A wide range of phones.
- Video clips filmed by hand in ordinary rooms. The video tool is limited to three motions because those are the ones whose numbers matched known values on real test clips.

## Known limits

- The microphone and camera need the app opened from its own web address, with permission allowed.
- Sound tools handle one note at a time. Speech has no single formula.
- Fast motion blurs on video, and cluttered backgrounds make the object harder to follow.
- Progress, settings and saved creations are kept in the browser on one phone only.

## Running it

The whole app is one file, `formula-play.html`. Open it in a browser, or host it on any static site. No build step and no server are needed.

## Built by

Tejashwar Reddy Vuyyuru

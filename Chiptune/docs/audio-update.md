# Audio update 1.1.1

DC removal, increased output gain and bounded peak compression improve the four-voice music signal. All nine scores, original player controls and the default volume remain. The oscilloscope shows the unprocessed score mix. The new output helper is included locally, so builds use the existing pinned upstream SDK.

Validation uses the actual C++ audio backend and native Rev0 builds. Digital
levels and source checks do not establish measured acoustic loudness or
physical timer margin. These releases retain each public repository's
existing build and save setup; workspace console builds also included a
separate SD-save overlay that is not part of this audio change.

## Release build validation

Built against the clean upstream SDK at
`e1f8d05940ddb7bbef89c13326da75c003f02904` with GCC 16.2.

```text
Chiptune: build
flash (sections): 38768 B
image: 39068 B of 50944 (save pages free: 2; two need <= 50432)
static RAM: 12368 B of 18416 (stack 2048 B separate)
```

18 rendered audio files match the tested workspace PCM byte for byte.

All nine scores pass three-loop note, timing and tuning checks; player controls,
exact mute and pause/resume pass.

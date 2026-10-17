# Audio rights

The root [MIT license](../LICENSE) covers repository documentation and the
original project logo. The audio files and their encoded/channel variants are
covered by [CC0 1.0 Universal](../LICENSES/CC0-1.0.txt), as described below.
Transcoding does not relicense third-party audio under MIT.

Sources and rights were reviewed on 2026-10-17. OpenGameArt identifies each
upstream recording below as CC0. Credit is retained even though CC0 does not
require attribution. The Stonefox dedicates the original frequency-sweep signal
and any copyright held in its generation to CC0, to the extent permitted by law;
the CC0 fallback license applies where necessary. No endorsement is implied.

Upstream originals, conversion scripts and working files are not stored here.

## Processing

- Each excerpt is three seconds and converted to 48,000 Hz stereo before the
  mono variant is derived. Mono is the arithmetic mean of left and right.
- Both profiles use the same excerpt and processing. Stereo preserves the
  source channels; mono is a downmix rather than a separate recording.
- Apply 20 ms linear fades at both ends. Scale the stereo peak to -6 dBFS,
  retaining that gain for mono, then quantize to signed 16-bit PCM.
- WAV and FLAC preserve those processed PCM samples exactly. The three sourced
  recordings are already lossy Vorbis; lossless conversion does not recover
  information removed by their original encoding.
- MP3 uses libmp3lame at 96 kb/s mono or 160 kb/s stereo. M4A uses FFmpeg AAC-LC
  at the same bitrates, with faststart container layout.
- Ogg Vorbis uses libvorbis quality 4. Opus uses libopus with VBR, the audio
  application setting, 64 kb/s mono or 96 kb/s stereo. FLAC uses level 8.
- Source metadata, cover art, video, subtitles and chapters are omitted.
  Standard container, encoder and codec-delay metadata may remain.
- Each processed input has 144,000 sample frames. The encoded duration is
  nominally three seconds; Opus includes pre-skip in its container duration,
  and AAC decoding can expose final frame padding. Exact decoded sample counts
  are guaranteed here only for WAV and FLAC.

## Original recordings

### birdsong

**Birdsong** - CC0-1.0

Credit: isaiah658. The source page lists the recording under CC0.

[Source and rights evidence](https://opengameart.org/content/ambient-bird-sounds) | [Upstream original](https://opengameart.org/sites/default/files/birds-isaiah658_0.ogg)

Original: 48,000 Hz, 2 channels, vorbis,
30.688250 seconds, 544,669 bytes. Retrieved 2026-10-17.
Excerpt: 0.000 to 3.000 seconds on the source playback clock.

Original SHA-256:

`359e4e3f9da9d75aac64cede511c7e3ef8b461f9d9f8c230f8f80e44c4b3e35f`

### rain

**Rain** - CC0-1.0

Credit: Ove Melaa. The source page lists the recording under CC0.

[Source and rights evidence](https://opengameart.org/content/rain-ambient-not-loopable-2-versions-available) | [Upstream original](https://opengameart.org/sites/default/files/Ove%20Melaa%20-%20Rainy%20%28NOT%20loopable%29.ogg)

Original: 44,100 Hz, 2 channels, vorbis,
80.677075 seconds, 1,633,276 bytes. Retrieved 2026-10-17.
Excerpt: 5.000 to 8.000 seconds on the source playback clock.

Original SHA-256:

`5083851776c2b3ff56b81550672d7f697efcdb88f605f83402d7dfc91c56b476`

### soft-piano

**Soft piano** - CC0-1.0

Credit: Tozan. The source page lists the recording under CC0.

[Source and rights evidence](https://opengameart.org/content/pianosoft8) | [Upstream original](https://opengameart.org/sites/default/files/softpiano8.ogg)

Original: 44,100 Hz, 2 channels, vorbis,
122.729002 seconds, 2,328,204 bytes. Retrieved 2026-10-17.
Excerpt: 5.000 to 8.000 seconds on the source playback clock.

Original SHA-256:

`273e511fcfa981642c6f40f5561f84f3595dcfaab0ae67101e22ab3da394f08d`

## frequency-sweep

**Frequency sweep** - CC0-1.0

Credit: The Stonefox. An original generated test signal, with no third-party
recording, instrument samples or composition.

The three-second source has 144,000 stereo sample frames at 48,000 Hz. The left
channel sweeps linearly from 300 to 3000 Hz and the right from 3000 to 300 Hz.
Each channel uses `sin(2*pi*(f0*t + (f1-f0)*t*t/6))` at `t = sample_index/48000`,
then the shared fades, peak scaling and PCM quantization above. The mono sample
is the average of the two channels. This is a swept test tone, not music.

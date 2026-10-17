# Audio samples

Four subjects across nature, music and test signals, each in **mono and stereo**
at **48,000 Hz**. Every excerpt is nominally **three seconds**, encoded in six
formats: **48 files**, 6,200,131 bytes total (5.91 MiB).
The largest file is 576,078 bytes; every file is below 600 KB.

[Repository usage](../README.md) | [Credits and rights](RIGHTS.md)

## Formats and codecs

| Format | Codec | Encoding | Files |
| --- | --- | --- | ---: |
| [WAV](wav/README.md) | PCM signed 16-bit little-endian | 16-bit PCM | 8 |
| [FLAC](flac/README.md) | FLAC | Lossless, 16-bit PCM, compression level 8 | 8 |
| [MP3](mp3/README.md) | MPEG-1 Audio Layer III | 96 kb/s mono; 160 kb/s stereo | 8 |
| [M4A](m4a/README.md) | AAC-LC in an MPEG-4 audio container | 96 kb/s mono; 160 kb/s stereo | 8 |
| [Ogg Vorbis](ogg/README.md) | Vorbis in Ogg | Variable bitrate, quality 4 | 8 |
| [Opus](opus/README.md) | Opus in Ogg | Variable bitrate, 64 kb/s mono; 96 kb/s stereo | 8 |

All formats use the same processed PCM for a given subject/channel layout.
WAV and FLAC decode to exactly 144,000 sample frames. Lossy formats can differ
in waveform, priming and final padding; AAC decoding can expose a partial final
frame, and Opus container duration includes pre-skip. Use timestamps and codec
metadata when testing precise playback length.

The sourced recordings are CC0. The generated frequency sweep is also dedicated
to CC0. Original credits and processing are recorded in [audio rights](RIGHTS.md).
These short samples are useful for loading, playback and codec smoke tests;
they are not a comprehensive codec conformance suite.

## Samples

Links below open the MP3 fixtures. Each format index includes both channel
layouts and their file sizes; playback support depends on your browser/player.

### Birdsong

Nature excerpt. Credit: isaiah658.

[Mono MP3](mp3/nature/birdsong-48000hz-mono.mp3) | [Stereo MP3](mp3/nature/birdsong-48000hz-stereo.mp3)

[WAV](wav/README.md#birdsong) | [FLAC](flac/README.md#birdsong) | [MP3](mp3/README.md#birdsong) | [M4A](m4a/README.md#birdsong) | [Ogg Vorbis](ogg/README.md#birdsong) | [Opus](opus/README.md#birdsong)

[Source and rights](RIGHTS.md#birdsong)

### Rain

Nature excerpt. Credit: Ove Melaa.

[Mono MP3](mp3/nature/rain-48000hz-mono.mp3) | [Stereo MP3](mp3/nature/rain-48000hz-stereo.mp3)

[WAV](wav/README.md#rain) | [FLAC](flac/README.md#rain) | [MP3](mp3/README.md#rain) | [M4A](m4a/README.md#rain) | [Ogg Vorbis](ogg/README.md#rain) | [Opus](opus/README.md#rain)

[Source and rights](RIGHTS.md#rain)

### Soft piano

Music excerpt. Credit: Tozan.

[Mono MP3](mp3/music/soft-piano-48000hz-mono.mp3) | [Stereo MP3](mp3/music/soft-piano-48000hz-stereo.mp3)

[WAV](wav/README.md#soft-piano) | [FLAC](flac/README.md#soft-piano) | [MP3](mp3/README.md#soft-piano) | [M4A](m4a/README.md#soft-piano) | [Ogg Vorbis](ogg/README.md#soft-piano) | [Opus](opus/README.md#soft-piano)

[Source and rights](RIGHTS.md#soft-piano)

### Frequency sweep

An original rising/falling test signal with distinct left and right channels.

[Mono MP3](mp3/signals/frequency-sweep-48000hz-mono.mp3) | [Stereo MP3](mp3/signals/frequency-sweep-48000hz-stereo.mp3)

[WAV](wav/README.md#frequency-sweep) | [FLAC](flac/README.md#frequency-sweep) | [MP3](mp3/README.md#frequency-sweep) | [M4A](m4a/README.md#frequency-sweep) | [Ogg Vorbis](ogg/README.md#frequency-sweep) | [Opus](opus/README.md#frequency-sweep)

[Source and rights](RIGHTS.md#frequency-sweep)

## Naming

```text
audio/<format>/<category>/<subject>-<sample-rate>hz-<mono-or-stereo>.<extension>
```

For example, `birdsong-48000hz-stereo.mp3` has a 48,000 Hz sample rate and two
channels. `birdsong-48000hz-mono.mp3` has the same sample rate and one channel.
WAV/FLAC use 16-bit PCM; lossy codec bitrates are listed above rather than encoded
into a misleading bit-depth label.

## Use a file

```text
audio/mp3/nature/birdsong-48000hz-stereo.mp3
```

```text
https://raw.githubusercontent.com/thestonefox/media-fixtures/main/audio/mp3/nature/birdsong-48000hz-stereo.mp3
```

Replace `main` with a full commit SHA for a stable URL. Download files or clone
the repository; no tools or dependencies are needed to use the fixtures.

## Size policy

Keep excerpts short and every audio fixture below 1 MB. The current collection
is under 7 MB total and needs no Git LFS. Keep upstream originals, generation
scripts and temporary conversion files outside the repository.

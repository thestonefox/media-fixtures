# Video audio and subtitle tracks

Moon orbit at **320 x 180 landscape**, **15 fps**, nominally **three seconds**.
The existing NASA video is combined with our CC0 audio fixtures and original
CC0 caption text. These are added test soundtracks, not location sound.

[Video gallery](README.md) | [Credits and rights](RIGHTS.md#added-audio-and-subtitles)

## Variants

- `with-audio`: one stereo piano soundtrack, no embedded subtitles.
- `multi-audio`: two separate stereo tracks: piano first, frequency sweep
  second. They are alternatives to select, not mixed together.
- `with-subtitles`: one stereo piano soundtrack and selectable English and
  Spanish captions. MKV also has an English ASS track with italic styling.

The video stream is copied from the existing silent fixture of that format.
Each audio stream is 48,000 Hz stereo. AAC/Opus/Vorbis priming and padding
can make timestamps and decoded sample counts exceed the nominal duration.

## Containers and codecs

| Container | Video | Audio | Embedded subtitles |
| --- | --- | --- | --- |
| MP4 / MOV | H.264 | AAC-LC, 128 kb/s per track | Two MPEG-4 Timed Text (`mov_text`) tracks |
| MKV | H.264 | AAC-LC, 128 kb/s per track | English SubRip, Spanish SubRip, English ASS |
| WebM | VP9 | Opus, 96 kb/s VBR per track | English and Spanish WebVTT |
| AVI | Motion JPEG | PCM signed 16-bit little-endian | Sidecars only in this collection |
| OGV | Theora | Vorbis, quality 4 VBR per track | Sidecars only in this collection |

The audio track order is always piano, then sweep where present. Track labels
identify each sound. `zxx` means no linguistic content; MOV and AVI do not
retain that audio language tag in these files. Subtitle languages are `eng`
and `spa`. MP4/MOV set the first subtitle track as default; MKV and WebM do
not mark a subtitle track as default. The piano audio track is marked default
where the container preserves it; AVI and OGV do not expose that flag.

Track selection and embedded subtitle support depend on the player. Some web
players expose only the first audio track or require separate WebVTT subtitles.
A media player with track controls is useful for checking all alternatives.

## Downloads

| Format | One audio track | Two audio tracks | Embedded subtitles |
| --- | --- | --- | --- |
| MP4 | [68,552 bytes](mp4/space/moon-orbit-320x180-landscape-with-audio.mp4) | [118,455 bytes](mp4/space/moon-orbit-320x180-landscape-multi-audio.mp4) | [69,907 bytes](mp4/space/moon-orbit-320x180-landscape-with-subtitles.mp4) |
| WEBM | [56,988 bytes](webm/space/moon-orbit-320x180-landscape-with-audio.webm) | [109,491 bytes](webm/space/moon-orbit-320x180-landscape-multi-audio.webm) | [57,582 bytes](webm/space/moon-orbit-320x180-landscape-with-subtitles.webm) |
| MOV | [68,603 bytes](mov/space/moon-orbit-320x180-landscape-with-audio.mov) | [118,610 bytes](mov/space/moon-orbit-320x180-landscape-multi-audio.mov) | [70,094 bytes](mov/space/moon-orbit-320x180-landscape-with-subtitles.mov) |
| MKV | [68,011 bytes](mkv/space/moon-orbit-320x180-landscape-with-audio.mkv) | [117,153 bytes](mkv/space/moon-orbit-320x180-landscape-multi-audio.mkv) | [69,479 bytes](mkv/space/moon-orbit-320x180-landscape-with-subtitles.mkv) |
| AVI | [760,280 bytes](avi/space/moon-orbit-320x180-landscape-with-audio.avi) | [1,341,396 bytes](avi/space/moon-orbit-320x180-landscape-multi-audio.avi) | Not included |
| OGV | [69,129 bytes](ogv/space/moon-orbit-320x180-landscape-with-audio.ogv) | [86,407 bytes](ogv/space/moon-orbit-320x180-landscape-multi-audio.ogv) | Not included |

All 16 additions total 3,250,137 bytes (3.10 MiB). The entire video collection
remains below 16 MB, with every video below 2 MB.

## Separate subtitle files

SRT is plain timed text, WebVTT is a web caption format, and ASS adds styles
and positioning. The ASS example italicizes the second cue. All are UTF-8.
The two captions are **0.200-1.300** and **1.500-2.800** seconds; English and
Spanish describe the same events. None are burned into the video pixels.

| Format | English | Spanish |
| --- | --- | --- |
| SubRip (SRT) | [English](subtitles/srt/moon-orbit-320x180-landscape-with-audio.en.srt) | [Spanish](subtitles/srt/moon-orbit-320x180-landscape-with-audio.es.srt) |
| WebVTT (VTT) | [English](subtitles/vtt/moon-orbit-320x180-landscape-with-audio.en.vtt) | [Spanish](subtitles/vtt/moon-orbit-320x180-landscape-with-audio.es.vtt) |
| Advanced SubStation Alpha (ASS) | [English](subtitles/ass/moon-orbit-320x180-landscape-with-audio.en.ass) | [Spanish](subtitles/ass/moon-orbit-320x180-landscape-with-audio.es.ass) |

Sidecar basenames match the `with-audio` clips, with a language suffix.
Some players load matching sidecars automatically; others require manual
selection. Copy a subtitle beside the video when the player requires it. The
same cue times also apply to the silent, multi-audio and embedded-subtitle
Moon-orbit fixtures, with small container timing shifts from audio priming.

ASS names Arial without embedding a font; players can substitute another
font. Identical appearance across platforms is not guaranteed. MP4/MOV timed
text and WebVTT examples carry the plain captions, not ASS styling.

## Format references

- [FFmpeg subtitle format support](https://www.ffmpeg.org/general.html#Subtitle-Formats).
- [Matroska subtitle storage](https://www.matroska.org/technical/subtitles.html).

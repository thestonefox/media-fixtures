# Video rights

The root [MIT license](../LICENSE) covers repository documentation. Each clip,
its animated preview and all container/size variants retain the source rights
below. Transcoding does not relicense third-party footage under MIT.

Sources and rights were reviewed on 2026-10-17. Bird and waterfall footage were
dedicated under [CC0 1.0 Universal](../LICENSES/CC0-1.0.txt) by their uploaders.
NASA footage is public domain in the United States; other jurisdictions may
differ. The wave simulation was released by its author into the public domain,
with an unconditional permission fallback where dedication is not possible.
No endorsement, trademark or personality rights are granted.

Only short, silent, resized derivatives are stored here. Upstream originals,
conversion scripts and working files are not part of this repository. All video
containers of a subject use the same three-second excerpt. GIF variants sample
the same interval at a lower frame rate for compact previews.

## Processing

- Video: three seconds, 15 fps, square pixels. Every filename records the exact
  width x height and orientation. See the [resolution table](README.md#resolutions).
  Native HD frames are 1280 x 720 landscape (Moon orbit) and 720 x 1280 portrait
  (bird). Lower-resolution sources are not upscaled.
- GIF: three seconds, 5 fps, 128-colour global palette, Bayer dithering, looping.
- Aspect ratio and framing are retained; the shorter edge is rounded to an even
  pixel count for codec compatibility. There is no crop or upscale.
- Each source excerpt is normalized once to eight-bit YUV 4:2:0. Variants are
  encoded from those same frames; MP4, MOV and MKV share the H.264 bitstream.
- H.264: libx264, baseline profile, CRF 28, slow preset, 15-frame GOP, no B-frames.
  MP4 and MOV are arranged for progressive download with faststart.
- VP9: libvpx-vp9, CRF 34, unconstrained bitrate, good deadline, CPU-used 2.
- Motion JPEG: quality 6, full-range YUV 4:2:0; the HD bird uses quality 10
  to stay below 2 MB. Theora: quality 5.
- Audio, subtitles, source metadata and chapters are removed. Container-required
  metadata and FFmpeg encoder identification remain. Lossy colours vary by codec.

The quoted start/end times below refer to each downloaded source's playback
clock, not real elapsed time in time-lapse or simulated scenes.

## earth-rotation

**Earth rotation** - LicenseRef-Public-Domain

Credit: NASA/JPL.

NASA/JPL Galileo flyby imagery (PIA00114); the source page records
public-domain status for this NASA work.

[Source and rights evidence](https://commons.wikimedia.org/wiki/File:Earth_rotation_during_Galileo_flyby_(PIA00114).webm) | [Upstream original](https://upload.wikimedia.org/wikipedia/commons/8/87/Earth_rotation_during_Galileo_flyby_%28PIA00114%29.webm)

Original: 480 x 360 pixels,
22.956 seconds, 1,230,270 bytes. Retrieved 2026-10-17.
Excerpt: 6.000 to 9.000 seconds; output is silent.

Original SHA-256:

`d70f697ecca7b8b624e802405aad5759278fe87c63d68f6472afb31d6feb36d2`

## bird-on-ledge

**Bird on a ledge** - CC0-1.0

Credit: Yourusernamewillbepublic2.

The author identifies this as their own work and dedicates it under CC0 1.0.

[Source and rights evidence](https://commons.wikimedia.org/wiki/File:Cute_Colorful_Bird_on_Walking_on_Ledge.webm) | [Upstream original](https://upload.wikimedia.org/wikipedia/commons/4/43/Cute_Colorful_Bird_on_Walking_on_Ledge.webm)

Original: 720 x 1280 pixels,
21.763 seconds, 13,426,030 bytes. Retrieved 2026-10-17.
Excerpt: 3.000 to 6.000 seconds; output is silent.

Original SHA-256:

`8b8030f05c7f13e6040ea1ea4f7182984dece53968c3116859838078e68a9b5b`

## misty-waterfall

**Misty waterfall** - CC0-1.0

Credit: BhotaRohit.

The author identifies this as their own work and dedicates it under CC0 1.0.

[Source and rights evidence](https://commons.wikimedia.org/wiki/File:Water_flowing_strem.webm) | [Upstream original](https://upload.wikimedia.org/wikipedia/commons/c/c9/Water_flowing_strem.webm)

Original: 478 x 850 pixels,
13.806 seconds, 6,001,205 bytes. Retrieved 2026-10-17.
Excerpt: 1.000 to 4.000 seconds; output is silent.

Original SHA-256:

`5652e6490bea85dfb7a1da05e00fc7f3d8cc2cbd54790c03a48223f2256bc3d1`

## shallow-water-waves

**Shallow-water waves** - LicenseRef-Public-Domain

Credit: Dan Copsey; WebM conversion by Nick Birse.

Dan Copsey released the simulation into the public domain worldwide, with
unconditional permission where public-domain dedication is not possible.

[Source and rights evidence](https://commons.wikimedia.org/wiki/File:Shallow_water_waves.webm) | [Upstream original](https://upload.wikimedia.org/wikipedia/commons/f/fc/Shallow_water_waves.webm)

Original: 491 x 258 pixels,
30.000 seconds, 800,289 bytes. Retrieved 2026-10-17.
Excerpt: 2.000 to 5.000 seconds; output is silent.

Original SHA-256:

`ca2485547445112e4ed86daf388ee016a61bf094046a27e565dbae6614228b8d`

## moon-orbit

**Moon orbit** - LicenseRef-Public-Domain

Credit: NASA Scientific Visualization Studio; Ernie Wright (USRA), Laurence Schuler and Ian Jones (ADNET Systems, Inc.).

The Commons source records this NASA visualization as public domain in the
United States. Other jurisdictions may differ. The original is native 1080p;
the HD fixture is downscaled to 1280 x 720 rather than enlarged.

[Source and rights evidence](https://commons.wikimedia.org/wiki/File:Moon_Essentials-_Orbit_(SVS5326_-_moon_orbit_simple_1080p30).webm) | [NASA source](https://svs.gsfc.nasa.gov/5326/) | [Upstream original](https://upload.wikimedia.org/wikipedia/commons/d/de/Moon_Essentials-_Orbit_%28SVS5326_-_moon_orbit_simple_1080p30%29.webm)

Original: 1920 x 1080 pixels,
90.000 seconds, 9,143,359 bytes. Retrieved 2026-10-17.
Excerpt: 10.000 to 13.000 seconds; output is silent.

Original SHA-256:

`65ec4514649374c4ad87c6b99fa94cf2d9fa91e7a37e72f145d43979cfb6d854`

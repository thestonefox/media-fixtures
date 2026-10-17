# Media Fixtures <img src="assets/media-fixtures.svg" width="157" height="36" align="top" alt="Images, video, audio and fonts">

Freely reusable media files in different formats and sizes for testing and demos. Images and short videos are available now; audio and fonts can be added later.

## Media

<table>
  <tr>
    <td valign="top">
      <h3><a href="images/README.md">Images</a></h3>
      <table>
        <tr><th>Format</th><th>Files</th></tr>
        <tr><td><a href="images/png/README.md">PNG</a></td><td align="right">75</td></tr>
        <tr><td><a href="images/jpg/README.md">JPEG</a></td><td align="right">75</td></tr>
        <tr><td><a href="images/gif/README.md">GIF</a></td><td align="right">75</td></tr>
        <tr><td><a href="images/bmp/README.md">BMP</a></td><td align="right">75</td></tr>
        <tr><td><a href="images/webp/README.md">WebP</a></td><td align="right">75</td></tr>
        <tr><td><a href="images/avif/README.md">AVIF</a></td><td align="right">75</td></tr>
      </table>
    </td>
    <td valign="top">
      <h3><a href="videos/README.md">Videos</a></h3>
      <table>
        <tr><th>Format</th><th>Files</th></tr>
        <tr><td><a href="videos/mp4/README.md">MP4</a></td><td align="right">12</td></tr>
        <tr><td><a href="videos/webm/README.md">WebM</a></td><td align="right">12</td></tr>
        <tr><td><a href="videos/mov/README.md">MOV</a></td><td align="right">12</td></tr>
        <tr><td><a href="videos/mkv/README.md">MKV</a></td><td align="right">12</td></tr>
        <tr><td><a href="videos/avi/README.md">AVI</a></td><td align="right">12</td></tr>
        <tr><td><a href="videos/ogv/README.md">OGV</a></td><td align="right">12</td></tr>
        <tr><td><a href="videos/gif/README.md">Animated GIF</a></td><td align="right">10</td></tr>
      </table>
    </td>
  </tr>
</table>

Three-second silent clips, with full **width x height** and orientation in every
filename. HD examples include **1280 x 720 landscape** and **720 x 1280 portrait**.
The complete motion collection is under 13 MB, with every file below 2 MB.
GIF previews stay small. See the [video resolutions](videos/README.md#resolutions).

## Use a file

Download a media file or clone the repo. There is nothing to install or run.
Local files work offline; remote URLs require a connection.

```text
images/png/animals/cat-on-couch-256.png
```

Raw URL:

```text
https://raw.githubusercontent.com/thestonefox/media-fixtures/main/images/png/animals/cat-on-couch-256.png
```

Replace `main` with a full commit SHA when you need a stable fixture URL.
Absolute local paths work like any other file on your machine.

## Sizes and formats

| Type | Dimensions | Timing |
| --- | --- | --- |
| Image | 64, 128, 256, 512, 1024 pixels on the longest edge | Static |
| Video | Full width x height; see [resolutions](videos/README.md#resolutions) | 3 seconds, 15 fps |
| Animation | Small width x height variants listed in the [video gallery](videos/README.md#resolutions) | 3 seconds, 5 fps |

Image filenames use `images/<format>/<category>/<subject>-<size>.<extension>`.
Video and animated GIF filenames use:

```text
videos/<format>/<category>/<subject>-<width>x<height>-<orientation>.<extension>
```

For example, `bird-on-ledge-720x1280-portrait.mp4` is **720 pixels wide and
1280 pixels tall**. `moon-orbit-1280x720-landscape.mp4` is **1280 pixels wide
and 720 pixels tall**. Dimensions describe the actual frame, not a `p` label.

Aspect ratio and framing are preserved. Video dimensions use an even shorter
edge for codec compatibility; media is not square-cropped.
Grace Hopper's smaller original is upscaled for the largest variants.

PNG and WebP are lossless and preserve full alpha. AVIF preserves full
alpha, with lossy colour for opaque images. JPEG and BMP use a white
background for transparency. GIF uses a palette and binary transparency:
alpha below 128 is transparent, and other partial alpha is white-matted.
All files under `images/` are static, including GIF and WebP.

## Rights

Credits, source links and public-domain/CC0 evidence are recorded in
[image rights](images/RIGHTS.md) and [video rights](videos/RIGHTS.md).
The [MIT license](LICENSE) covers repository documentation and the original
project logo. It does not relicense third-party media.

# media-fixtures

Freely reusable media files in different formats and sizes for testing
and demos. Images now; other media types can be added later.

**15 subjects | 7 categories | 6 formats | 5 sizes | 450 image files**

[Browse the gallery](images/README.md) | [Credits and rights](images/RIGHTS.md)

| Format | Files |
| --- | --- |
| [PNG](images/png/README.md) | 75 |
| [JPEG](images/jpg/README.md) | 75 |
| [GIF](images/gif/README.md) | 75 |
| [BMP](images/bmp/README.md) | 75 |
| [WebP](images/webp/README.md) | 75 |
| [AVIF](images/avif/README.md) | 75 |

Each format folder contains nature, people, objects, animals, space,
illustrations and patterns, with **at least two different subjects per category**.
Every subject is the same image across all formats and sizes.

## Use a file

Download an image or clone the repo. There is nothing to install or run.
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

Filenames follow `images/<format>/<category>/<subject>-<size>.<extension>`.
Sizes are **64, 128, 256, 512 and 1024** pixels on the longest edge.
Aspect ratio and framing are preserved; images are not square-cropped.
Grace Hopper's smaller original is upscaled for the largest variants.

PNG and WebP are lossless and preserve full alpha. AVIF preserves full
alpha, with lossy colour for opaque images. JPEG and BMP use a white
background for transparency. GIF uses a palette and binary transparency:
alpha below 128 is transparent, and other partial alpha is white-matted.
All files are static images, including GIF and WebP.

## Rights

Image credits, source links and public-domain/CC0 evidence are recorded
in [image rights](images/RIGHTS.md). The [MIT license](LICENSE) covers
repository documentation and does not relicense third-party images.

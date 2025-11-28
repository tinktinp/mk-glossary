# Mortal Kombat Glossary

A glossary of things related to Mortal Kombat, with a particular focus on the arcade era,
and on internals and ROM hacking related topics.

## The Glossary
### A
### B
#### BG
"Brian Glynn", the actor and bodybuilder who played Shao Khan
in MKII and 3. (Khan was voiced by Steve Ritchie.)

Khan is also referred to as `SK` and `BOSS`.

For example, `BOSS1.IMG`'s first sprite is named `BGSTANCE1`.

#### Big Goro

Kintaro.

### C

#### CLUT or CLT

Color Look-Up Table. This is another name for a palette.

The N64 MKT source code contains tables with the suffix `_CLT`.
These `CLT` tables are not themselves palettes, they a table
of pointers, and each pointer points to a palette.

### D
### E
### F
### G
### H
#### HH, Hathead, Hathed

Kung Lao in Mortal Kombat 2.

For example, the file `HATHED1.IMG` contains a sprite named `TMSTANCE1`.

### I

#### Indexed Color Mode

Raster images consist of a 2d grid of pixels. Each pixel is a number.

If the number refers to an entry in a palette, then number is
said to be an "index" into the palette, and the image is said
to be in index color mode.

Common image formats that support palettes are GIFs and PNGs.

This is sometimes called called 8-bit mode, because each pixel takes up 8 bits (one byte).

This gets a bit confusing, because 24-bit RGB and 32-bit RGBA images are also sometimes referred to as having "8-bit channels", because each of the Red, Green, Blue, and Alpha channels takes up 8 bits per pixel. 

For arcade era Mortal Kombat games, the palettes are often less than 8-bits.

### J
### K
### L
### M
### N
### O

### P

#### Palette
General meaning: A set of colors used in a composition. 

Usually we mean a table of colors associated with a particular image or set of images. Those images use "indexed" color mode.

[GIMP](https://www.gimp.org) makes a distinction between a [palette](https://docs.gimp.org/3.0/en/gimp-concepts-palettes.html) and a [colormap](https://docs.gimp.org/3.0/en/gimp-concepts-palettes.html#idm4763).

### Q
### R
### S
#### Son of Goro

Kintaro.

Kintaro is not Goro's son in the storyline, but is referred to
as such in the MKII source code and assets. This is often shortened to just "Goro".


### T
#### TM
"The Monk". Kung Lao in MKII.

For example, the file `HATHED1.IMG` contains a sprite named `TMSTANCE1`.

### U
### V
### W
### X
### Y
### Z
# Sprite and graphics formats for Mortal Kombat Trilogy PSX/PC/Saturn

## ImHex `.hexpat` files

There are pattern files for [ImHex](https://imhex.werwolv.net/) here: https://github.com/tinktinp/hexpat

## The files


The various CD versions of the game contain mostly the same files, sometimes in different directories. 

The Saturn version is currently unsupported by img-viewer. It seems to be in the same format and with files the same size as the others, but is in big endian format instead of little endian.

Most characters have 3 `.dat` files, a regular one, a `bq` one and a `fat`(ality) one. They mostly contain the same sprites but with a handful of differences.

The `bq` and `fat` versions also contain some image headers with duplicate data offsets. In these cases, only the last one seems to have the correct width/height.

Some backgrounds have two files, but they also seem to have a lot of the same sprites.

On Playstation the v1.1 disc contains these files:

Audio files:
```
SOUND
    SHAOKAHN.DAT
    BARAKA.DAT
    KANO.DAT
    RAIDEN.DAT
    SHANG.DAT
    MALE4.DAT
    KABAL.DAT
    MALE1.DAT
    KLAO.DAT
    STRYKER.DAT
    MALE3.DAT
    FNINJAS.DAT
    MALE2.DAT
    GORO.DAT
    ROBOT.DAT
    FEMALE.DAT
    SONYA.DAT
    MOTARO.DAT
    LKANG.DAT
    INDIAN.DAT
    SHEEVA.DAT
    SINDEL.DAT
    SUBZERO.DAT
    JAX.DAT
    COMMON.DAT
    NINJAS.DAT
SOUNDB
    SUBWAYBG.DAT
    TOMB.DAT
    POOL.DAT
    HELL.DAT
    PIT3.DAT
    FOREST.DAT
    STARTUP.DAT
    SKDEATH.DAT
    MISCFLF.DAT
    JONCAGE.DAT

SOUND2
    SHAOKAHN.DAT
    KANO.DAT
    RAIDEN.DAT
    SHANG.DAT
    KABAL.DAT
    KLAO.DAT
    STRYKER.DAT
    MALE3.DAT
    FNINJAS.DAT
    ROBOT.DAT
    FEMALE.DAT
    SONYA.DAT
    MOTARO.DAT
    LKANG.DAT
    INDIAN.DAT
    SHEEVA.DAT
    SINDEL.DAT
    SUBZERO.DAT
    JAX.DAT
    COMMON.DAT
    NINJAS.DAT
```

Background "maps":
```
MAPS
    STEEL.MAP
    SPIRAL.MAP
    BATTLE.MAP
    THRONE.MAP
    ARMORY.MAP
    BANK.MAP
    PITCITY.MAP
    SUBWAY.MAP
    DOOR.MAP
    WATER.MAP
    ARENA.MAP
    TOWER.MAP
    HADES.MAP
    POOL.MAP
    LADDER.MAP
    ENDSTONE.MAP
    BRIDGE.MAP
    LOST.MAP
    GORO.MAP
    FOREST.MAP
    TOMB.MAP
    KUNGFU5.MAP
    SOUL.MAP
    GRAVE.MAP
    KUNGFU2.MAP
    DESERT.MAP
    BELL.MAP
    TEMPLE.MAP
    MK2BRIG.MAP
```

Background graphics:
```
BGND
    TOMB.DAT
    SOUL.DAT
    GRAVE.DAT
    KUNGFU5.DAT
    GOROBGND.DAT
    KUNGFU2.DAT
    DESERT.DAT
    BELL.DAT
    TEMPLE.DAT
    MK2BRIG.DAT
    HADES.DAT
    POOL.DAT
    LADDER.DAT
    BRIDGE.DAT
    LOST.DAT
    FOREST.DAT
    DOOR.DAT
    WATER.DAT
    ARENA.DAT
    SUBWAY.DAT
    TOWER.DAT
    STEEL.DAT
    BATTLE.DAT
    SPIRAL.DAT
    THRONE.DAT
    ARMORY.DAT
    BANK.DAT
    PITCITY.DAT
BGND2
    BANK2.DAT
    HADES2.DAT
    ENDSTONE.DAT
    STREET2.DAT
    BALC2.DAT
    SOUL2.DAT
    CAVE2.DAT
    ROOF2.DAT
    SUBWAY2.DAT
```

Character graphics:
```
CHARS1
    SHAOKAHN.DAT
    KUNGLAO.DAT
    BARAKA.DAT
    KANO.DAT
    RAIDEN.DAT
    CAGE.DAT
    SHANG.DAT
    FNINJA.DAT
    KABAL.DAT
    STRYKER.DAT
    GORO.DAT
    ROBOT.DAT
    NINJA.DAT
    OLDJAX.DAT
    KINTARO.DAT
    SONYA.DAT
    HATHEAD.DAT
    OLDRAID.DAT
    MOTARO.DAT
    INDIAN.DAT
    SHEEVA.DAT
    SINDEL.DAT
    SUBZERO.DAT
    JAX.DAT
    OLDKANO.DAT
    LIUKANG.DAT
CHARS2
    GOROBQ.DAT
    OLDJAXBQ.DAT
    SHAOKBQ.DAT
    CAGEBQ.DAT
    SHEBQ.DAT
    JAXBQ.DAT
    SONYABQ.DAT
    SWATBQ.DAT
    LIUBQ.DAT
    ROBOTBQ.DAT
    KUNGBQ.DAT
    FNINJABQ.DAT
    SHANGBQ.DAT
    NINJABQ.DAT
    KANOBQ.DAT
    UGMOBQ.DAT
    INDIANBQ.DAT
    MOTABQ.DAT
    OKANOBQ.DAT
    KABALBQ.DAT
    KINTBQ.DAT
    ORADBQ.DAT
    HHBQ.DAT
    TURKBQ.DAT
    RAIDENBQ.DAT
    LIABQ.DAT
CHARS3
    SHANGFAT.DAT
    ROBOFAT.DAT
    HHFAT.DAT
    OLDJFAT.DAT
    LIAFAT.DAT
    LIUFAT.DAT
    SUBZFAT.DAT
    KUNGFAT.DAT
    SGFAT.DAT
    KANOFAT.DAT
    RAIDFAT.DAT
    UGMOFAT.DAT
    GORO.DAT
    SHAOFAT.DAT
    INDFAT.DAT
    SONYAFAT.DAT
    KINTARO.DAT
    KABALFAT.DAT
    CAGEFAT.DAT
    MOTARO.DAT
    FNINJFAT.DAT
    SWATFAT.DAT
    ORADFAT.DAT
    OKANOFAT.DAT
    JAXFAT.DAT
    NINJAFAT.DAT
```

"Fluff":
```
FLUFF.BIN
```


Misc or unknown:

```
SLUS_003.30
STR0
    FILE01.IXA
    FILE00.IXA
    FILE02.IXA
    FILE03.IXA
SYSTEM.CNF
```

Animation tables (`anitab`s):
```
CODE
    FNINJA.BIN
    KABAL.BIN
    STRYKER.BIN
    GORO.BIN
    BARAKA.BIN
    KANO.BIN
    RAIDEN.BIN
    CAGE.BIN
    SHANG.BIN
    SHAOKAHN.BIN
    KUNGLAO.BIN
    OLDKANO.BIN
    LIUKANG.BIN
    OLDRAID.BIN
    MOTARO.BIN
    INDIAN.BIN
    SHEEVA.BIN
    SINDEL.BIN
    SUBZERO.BIN
    JAX.BIN
    KINTARO.BIN
    SONYA.BIN
    HATHEAD.BIN
    ROBOT.BIN
    NINJA.BIN
    OLDJAX.BIN
```


Ending graphics:
```
ENDING
    KANO.DAT
    RAIDEN.DAT
    JADE.DAT
    OKANO.DAT
    KITANA.DAT
    KABAL.DAT
    ST.DAT
    SWAT.DAT
    SMOKE.DAT
    SZ.DAT
    REPTILE.DAT
    LIA.DAT
    SONYA.DAT
    ORAD.DAT
    SEKTOR.DAT
    MOTARO.DAT
    CYRAX.DAT
    SCORPION.DAT
    INDIAN.DAT
    SHEEVA.DAT
    JAX.DAT
    SHAOK.DAT
    LK.DAT
    LAO.DAT
```

Stances graphics:
```
STANCES.DAT
```

A few movies / startup screens:
```
MOVIES
    AVALLGO2.STR
    LOGOSND.STR
    DRAGNSND.STR
```

Misc graphics:
```
LOGO.DAT
MISC.DAT
OPTIONBQ.DAT
PSELECT.DAT
TEXT.DAT
VERSUS.DAT
```



Main executable:
```
TRILOGY.EXE
```


Versus screen graphics:
```
VERSUS
    SONYAVS.DAT
    JAXVS.DAT
    MOTAROVS.DAT
    SWATVS.DAT
    GOROVS.DAT
    NINJVS.DAT
    CAGEVS.DAT
    OJAXVS.DAT
    LAOVS.DAT
    SHANGVS.DAT
    ROBOVS.DAT
    KANGVS.DAT
    TUSKVS.DAT
    INDVS.DAT
    ORAIDVS.DAT
    BARAVS.DAT
    OKANOVS.DAT
    KINTVS.DAT
    RAIDVS.DAT
    KANOVS.DAT
    KAHNVS.DAT
    FNINJVS.DAT
    LIAVS.DAT
    SZVS.DAT
    HHVS.DAT
    SGVS.DAT
```


## ImHex Patterns and Types

ImHex patterns look something like C or Rust.

See https://docs.werwolv.net/pattern-language/core-language/data-types for full details.

Instead of `int`s, it uses types such as `s16` or `u32`. (Which are a signed 16 bit integer, and an unsigned 32-bit integer).  

You can take several of these tyeps and give them names, and group them together to create a `struct`.

Humans only have a handful of short term memory slots. You can only keep a couple of things in your head at once. 

There's a "hack" to keep more things in your head at once: bundle up those things.

It's easier to think about a "Sprite" than to think about "four 16-bit integers (width, height, x and y offsets), a pointer or offset to some pixel data, and a palette". 

Whehter you call them "struct(ure)s" or "objects" or "records" or "tables", these aggregate types turn many pieces into one whole, and free up your human memory for other things. (Or maybe just another struct.)

## Format for graphics in `.DAT` character files
The `.dat` files are similar but a little different between the character sprites and the backgrounds.

You can see the code that handles this for img-viewer here: https://github.com/tinktinp/img-viewer/blob/a688d6d5/packages/image-viewer/src/asm/mktPcImageFile.ts


I will use the hexpat pattern files to help explain the format.

### Outline of file

```rust
struct MktPcCharacterFile {
    // The first 32 bits is the offset to the table of palettes
    // Alternativelym you can think of it as the length of everything before the palette section
    u32 offset_to_palette_section;

    // This is the offset to the "tables" section. 
    // Or it might be simpelr to think of it as the length of the
    // image headers section that immediately follows.
    u32 offset_to_tables_section;

    // An array of "ImageHeader"s
    // We don't get the number of items in the array, but we do get
    // its size in bytes.
    ImageHeader imageHeaders[while($ < offset_to_tables_section)];

    // This next section varies depending on the compression
    // method of the file
    u16 tables[while($ < (imageHeaders[0].imageOffset + 4))] @ offset_to_tables_section + 4;

    // Not shown here: the image data comes next

    // Finally, we have the table of palettes (as known as CLUTs, Color Look-Up Tables):
    PaletteList palette_section @ offset_to_palette_section + 4;

    // There is usually one final word at the end
    // It may be the size of the palette section but I'm
    // not certain.
};

// Place the above struct at offset "0", that is, this structure describes the file as a whole
MktPcCharacterFile mktPcCharacterFile @ 0x0;
```

This gives us the outline of the file.

#### An aside and alternative view

I don't know if the way I divided it up really matches how the original developers thought of it. Likely it doesn't. I'm starting to think that it should actually be thought of us two top level fields, more like:

```rust
struct MktPcCharacterFile {
    u32 imageSectionLen;
    ImageSection imageSection;

    u32 paletteSectionLen;
    PaletteSection paletteSection;
}
```

In this view, many of the fields I shown above are hidden within the `ImageSection`, but I pulled the `byteLength` field of the `PaletteList` up out of that struct and into this one.

### The Palette Table

The palette table is at the end of the file for character files.

For background files (not yet discussed), things are a little more complicated and there may be more than one.

First we define the palette section as a whole:
```rust
struct PaletteList {
    // The size of this section
    u32 byteLength;

    // A list of palettes
    Palette palettes[while(std::mem::read_unsigned($, 2) != 0x00)];
};
```

And then we have the palettes themselves:

```rust
struct Palette {
    // Number of entries in the palette
    // Note: each entry is two bytes, so size in bytes is twice this value!
    u16 paletteSize;

    // The palette data itself. Each entry is a 16 bit integer.
    // It's in a `5551` format, which means 5 bits for each color,
    // and 1 bit is not used.
    // Later you'll want to convert it to 24 bit RGB.
    u16 paletteData[paletteSize];
};
```

After all the palettes, there is a `u16` `00 00`, which you can think of as an empty palette. I'm using that to figure out the end of the list of palettes. But you could also use the `byteLength` if you prefer.


### Image Headers

The sprites are defined like this:

```
struct ImageHeader {
    // This is a 24 bit offset to the pixel data.
    u24 imageOffset;

    // Normally you don't see 24 bits by themselves,
    // you see a full 32 bits.
    // The remaining 8 bits are here. The `type::Hex`
    // is just a way to ask ImHex to display this value
    // in hex.
    type::Hex<u8> type;


    // Now we have the width and height. Very important,
    // but also pretty straight forward.
    u8 width;
    u8 height;

    // These next two fields are x and y offsets used when
    // this image is part of an animation.
    // These are signed, so they might appear as `FF FD`, for example, in your hex editor, which is just what `-3` looks like.
    s16 xOffset;
    s16 yOffset;

    // Finally we have the `paletteId`.
    // This is an index into the palettes array.
    // `0` is the first palette, `1` is the second one, and so on.
    u16 paletteId;
}; 
```

### Widths usually need to be padded

Usually the width given is the real width of the sprite that the
game wants to display.

But often that width is rounded up to a multiple of four when the image is stored in memory.

If you need to pad, but don't, then the image will look scrambled with sort of a diagonal pattern. That's true any time you get the width incorrect.

You'll often see that done like this:

```js
const paddedWidth = (width + 3) & ~3;
```

Since "3" is "11" in binary, another way to write that, least in Javascript, is:
```js
const paddedWidth = (width + 3) & ~0b11;
```

The `~` operator takes all the bits and flips them: `0`s become `1`s and `1`s become `0`s. So that turns into:

```js
const paddedWidth = (width + 3) & 0b1111_1111_1111_1100;

```

What this does is it sets the lowest two bits to zero, and the rest of the bits are unchanged. 

All of this is a fancy way to add `3`, then round down to the closest multiple of `4`.

See [What Is Bitwise And](./what-is-bitwise-and.md).

## The compression formats

You may be better off [reading the code](https://github.com/tinktinp/img-viewer/blob/a688d6d58ac35cd206e0da125275b03fbe0b29f6/packages/image-viewer/src/asm/decompressPc.ts).

There's three compression formats used, RLE (Run Length Encoding), BQ (block) and Huffman. Some backgrounds are not compressed, but use a tile format.

There's a class I use a lot called `BufferPtr`.

`BufferPtr` is a [Uint8Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array) and an offset. It has some methods to read and write bytes while adjusting the `offset`. It's designed to be used similar to how you might use a pointer in C with the `*(++out) = *(++in);` pattern that you sometimes see. 

### RLE

For RLE, there's a `tables` piece of metadata with two values, the `nBitsPerPixel` and the `nRLEBits`.

The first one, `nBitsPerPixel`, is used in the outer loop. This might be an actual pixel, or it might be `0`, which switches us into "zero run" mode.

Despite everything being named RLE, this ends up being more of a zero compression algorith. RLE usually allows runs of any value, but this version only allows runs of zeros.

The way the code in img-viewer handles the bit reading is kind of weird. It was the first one of these I implemented, and for later ones I came up with a `BitBuffer` class that works better and is more generic than the `rleHelper` and `RleState` used in this one.

The algorithm, at least as I implemented it, goes like this:

- Create an `inPtr` for the input buffer
- Create an output buffer with `width * height` bytes
- Initialize `nBitsPerPixel` to `tables[0]`
- Initilize `nRLEBits` from `tables[1]`
- While the output buffer isn't full:
    - Read some `nBitsPerPixel` into a `currByte` variable
    - If `currByte` is `0`:
        - initalize `nZeros` to `0`
        - while `currByte` is still `0`, read `nRLEBits` bits and set `currByte` to *that* value
            - each time we read a zero, that counts as "max zeros" zeros; increment `nZeros` by that amount
        - add the non-zero value of `currByte` to `nZeros`
        - append that many zeros to the output buffer
    - Otherwise, copy `currByte` to the output buffer

### BQ

TODO

For now you'll just have to read the code.

### Huffman

TODO

For now you'll just have to read the code.

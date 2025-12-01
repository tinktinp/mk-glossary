# Mortal Kombat Glossary

A glossary of things related to Mortal Kombat, with a particular focus on the arcade era,
and on internals and ROM hacking related topics.

## The Glossary
### A
#### A0, A1, A2, A3, A4, A5, A6, A7, A8, A9, A10, A11, A12, A13, A14, B0, B1, B2, B3, B4, B5, B6, B7, B8, B9, B10, B11, B12, B13, B14

These are the names of the registers in the TMS34010 CPU. 

They are used as parameters, and also as global variables.

In the ports, they often have global variables named after these registers, which allowed them to more directly translate the assembly language code to C. You'll also see them in some `struct`s.

#### AIL
[IBM Audio Interface Library (AIL2) by John Miles / Miles Design, Inc.](https://github.com/Tronix286/AIL2)

A library used in the DOS ports of Mortal Kombat.


#### Alone
A single player game. One player is **joy** and the other is **drone**.

*Alone is how to find me.*

#### AMODE
Attract Mode.

#### Ani
Animation.

#### anirate

Animation rate. 

#### Anitab
Animation table.

Every character has two `anitab`s. Each entry in the anitab is a pointer to an animation.

Each animation is itself a table/list/array, with each entry consisting of either a pointer to an animation frame, or else a special instruction. The game knows that anything below a certain value (100 or so) is an instruction and not a pointer.

Each animation frame is itself a list of images that are to be composed together.

Each image contains a width, height, x and y offsets, a pointer to the image data itself (which in the arcade is in bits and not bytes), a DMA control word (except in MK1), and sometimes a pointer to the palette.

#### Anthony Marquez
Also called Tony Marquez.
Played Kung Lao.

#### ASK_MR_DIFF

A function to check the current drone difficulty. This number increases as you climb the ladder.

#### Attract Mode

This is the mode that the game is in when no one is playing. It is trying to "attract" players, in order to make money for the arcade operator.

This is the mode that shows the story, character bios, CPU vs CPU fights, Rain the graveyard, ads for the CD and comic book, etc.


### B

#### Becky Gable
Female ninjas in UMK3.

#### BG
"Brian Glynn", the actor and bodybuilder who played Shao Khan
in MKII and 3. (Khan was voiced by Steve Ritchie.)

Khan is also referred to as `SK` and `BOSS`.

For example, `BOSS1.IMG`'s first sprite is named `BGSTANCE1`.

#### BH
Big Head. One of the MK3 fatalities.

#### Big Goro

Kintaro.

#### `.bin`

A common file extension, used for any kind of binary data.

In the arcade assets, `.bin` files are often pkzipped images, which are usually stored in the code roms rather than the gfx roms. After being zipped they are further processed with a Midway internal tool called `zip2bin`.

In MKT (PSX and PC), `.bin` files are anitabs. (The PC version doesn't seem to use them, as it also contains a copy of the anitabs in the `.exe` file.)

In MK3 assets, `.bin` files are the output of `psylink` and produced from `.o` files that are themselves the results of running an assembler on various files. (Note that even though an assembler and assembly is involved, these files usually only contain data and not code.)

There are also audio files with the `.bin` extension. 

#### BLD
Blood.

#### BLK
Block.

#### Box
Character selection box or portrait.


### C

#### Cage

1. Johnny Cage
2. Ribcage sprite (MK3)

#### CLUT or CLT

Color Look-Up Table. This is another name for a palette.

The N64 MKT source code contains tables with the suffix `_CLT`.
These `CLT` tables are not themselves palettes, they a table
of pointers, and each pointer points to a palette.

(Despite the similar spelling, it is almost completed unrelated to [anatomy](https://en.wiktionary.org/wiki/clitoris).)

#### Carlos Pesina
Played Raiden in first 3 MK games. Brother of Daniel Pesina.

#### CMOS

[CMOS](https://en.wikipedia.org/wiki/Nonvolatile_BIOS_memory)

CMOS can refer to the material that certain types of computer chips, [Complementary metal–oxide–semiconductor](https://en.wikipedia.org/wiki/CMOS). But it usually means the small amount of non-volatile storage (which often requires a battery in the real, vintage hardware), that the machines use to store settings, audits, etc. 

It's where the game stores whether the secret characters have been unlocked, how many times each character was chosen, what the overall difficulty is set to, the volume level, your initials, etc. 

All the other storage is either read-only, or volatile (loses its contents with the machine is turned off). 

Also called `NVRAM` or just `NV`.

#### Corpse
A dead body. In endurance matches, a "corpse" is the defeated first fighter that lays on the ground while fighting the second one.

#### CRT

[Cathode-ray tube](https://en.wikipedia.org/wiki/Cathode_ray_tube). The technology
used for TV screens from the 1930s until the late 2000s. Very heavy. As deep as they are wide adn tall.

They are relevant today because:
- they had a blurring effect, so the games looked different on them compared to LCDs
- the way the worked with their vertical and horizontal syncs was taken into account in the games' code

CRTs and TV signals at that time were analog, and didn't really have pixels in the same way that modern LCD displays do.

An electron gun fired electrons towards the viewer. The inside of the screen was coated in 3 different colors of phosphor, which glows when electrons hit it. The electron gun would sweep left to right, turn off briefly to move down a row, and then repeat. This brief time when it is off is called the horizontal sync.

Once it reaches the bottom, it turns off for a bit longer to return to the top left corner and begin the process again. This is know as the vertical sync. It is during this time that buffers are swapped (if doing double buffering). That way the CRT redraws an entire new frame, instead of switching to a new frame partly through the screen. (If you turn off vertical sync, you get "tearing".)

Many emulators today offer "CRT filters" to try to make games look better on modern displays. This produces an effect (which some people find unpleasant) [almost, but not quite, entirely *unlike*](https://en.wikipedia.org/wiki/Phrases_from_The_Hitchhiker%27s_Guide_to_the_Galaxy#Not_entirely_unlike) a real CRT.




### D
#### Danger, Danger
A warning when low on health.

https://www.youtube.com/watch?v=OWwOJlOI1nU

#### Daniel Pesina
Material artists who portrayed Johnny Cage as well as the male ninjas in the first two Mortal Kombat games.

- https://en.wikipedia.org/wiki/Daniel_Pesina
- https://masterpesina.com/


#### DBLO
Death Blow.

#### DFE
Distance From Edge. From the edge of the universe.

#### DFEOS
Distance From Edge Of Screen.

#### DMA
[Direct Memory Access](https://en.wikipedia.org/wiki/Direct_memory_access).

The Midway arcade machines have a special DMA or DMA2 chip that is used for drawing sprites (for doing block transfers from the gfx roms to video memory).

This site has a lot of details and references: https://fabiensanglard.net/nbajamte/

The DMA chip can also do things like handle zero compression (zcomp), flip the sprites, expand low bits-per-pixel (BPP), and a few other things. There's a ctrl (control) word associated with each sprite in MK2 or later that sets the BPP and zcomp settings. But the lower bits are set when doing the drawing operation since they are context dependent (such as flipping a sprite because you changed sides).


#### Death Blow
A fatality. Internally they are sometimes called "death blow"s, especially in the earlier games.

#### Dudes
People. `ALLDUDES.IMG` has the stances for the entire roster.

#### Drone

A fighter controlled by the game rather than by a player. The game's "AI" is usually contained in a file with "drone" in the name.

### E

#### Eddie Wong
Liu Kang in MK3.

#### EMP, Emperor

In MK2 we learn that Shao Khan is the ruler of Outworld. 

But in MK1, the game's assets use `EMP` and `EMPEROR` to refer to Shang Tsung.
Many sprites also use the prefix `YT`, with a palette named `YANG_P`.
There are also palettes named `EMP_P` and `EMP_FROZE_P`.

#### Endian
The order of the bytes. "Byte order".

See https://en.wikipedia.org/wiki/Endianness

In IMG files, little endian encoding is used. So if a sprite were 132 pixels tall (0x84 in hex), its height would be encoded as `84 00`, and if one were 10,000 pixels tall (0x2710 in hex), it would be encoded as `10 27`.  (When viewed in a hex editor.)

The Nintendo 64 uses big endian, so if the same fields were encoded for that platform, they would look like `00 84` and `27 10` in a hex editor.

Why groups of two digits? Each hex digit is only half a byte (called a "[nybble](https://en.wikipedia.org/wiki/Nibble)"), which means you need two of them to make a whole byte. That's why when you change the order of the bytes, you'll see the hex digits swap around in groups of two digits. 

The size of the field matters too. If we were writing 32 bit (4 byte) fields, we'd have either LE `84 00 00 00` or BE ``00 00 00 84`;

### F
#### FAT
Fatality.

#### FEMGORO
Female Goro, Sheeva.

#### FN, FNINJA
Female Ninja.
Kitana, Mileena, Jade, and Khameleon.

#### FX
Special effects.

### G
### H
#### HD
Head. Usually part of a "BOX" or "MUG".
#### HH, Hathead, Hathed

Kung Lao in Mortal Kombat 2.

For example, the file `HATHED1.IMG` contains a sprite named `TMSTANCE1`.

#### HO
Ho Sung Pak. Original actor of Liu Kang and (old) Shang Tsung.

Usually refers to Liu Kang in MK1 game assets, with `EMP` being used for Shang Tsung.

### I

#### Index

As a noun, an *index* is a number that tells you which entry in a table or element in an array you are after.

As a verb, *index* or *indexing* means to access an element of an array using an index.

If you have a datatype in some programming language that is an "array", which means it is sequence of multiple pieces of data of the same type, then you can select one element from the array by **indexing** it. 

```c
unsigned long myData[] = [10, 11, 12, 13, 14, 15]; // create an array of 6 `unsigned long`s

unsigned long firstElement = myData[0]; // arrays indexes usually start at 0, this assigns `10` to `firstElement`, at least in C
unsigned long someElement = myData[3]; // someElement gets the value `13`
```

If you see a variable named `i` used to index an array (usually in a `for` loop), that variable `i` is short for `index`, and is used to index the array.  

If the thing you are indexing is a table, that table is often called a **Look Up Table** or **LUT**.

An index might also be called an **offset**. 

An index is similar to a pointer. 

- An index is relative to whatever array or table it is used with, while a pointer is usually absolute
  - But if you think of all of memory as if it was one big array, then a pointer is just an index into that all-of-memory-array
- A pointer, if you look at its numeric value, is in bytes (or sometimes bits). An index is in *elements* and not bytes. 
  - In languages like `C`, pointer arithmetic is also in elements, so `myPtr += 1;` might actually add `4` to the numeric value of `myPtr`, if it points to 4 byte elements
  - This is important to pay attention to if you're jumping back and forth between a C and an assembly view, or if the C code uses typecasts and treats an array of `long`s or `word`s as an array of `char`s or `byte`s at times



#### Indexed Color Mode

Raster images consist of a 2d grid of pixels. Each pixel is a number.

If the number refers to an entry in a palette, then number is
said to be an "index" into the palette, and the image is said
to be in index color mode.

Common image formats that support palettes are GIFs and PNGs.

This is sometimes called called 8-bit mode, because each pixel takes up 8 bits (one byte).

This gets a bit confusing, because 24-bit RGB and 32-bit RGBA images are also sometimes referred to as having "8-bit channels", because each of the Red, Green, Blue, and Alpha channels takes up 8 bits per pixel. 

For arcade era Mortal Kombat games, the palettes are often less than 8-bits.

#### Indian
Nightwolf.

### J

#### JC
Johnny Cage.

#### John Parrish 
Played Jax.

#### John Turk
Unmasked Sub-Zero and Shang Tsung in MK3.
Male ninjas in UMK3 / MKT.


#### Joy
Joystick. The controller in the arcade.

`joy` is often used to mean "human player", as opposed to a "drone". 

`am_i_joy` checks if the current process is a human player (controller by a joystick or gamepad).

#### JX
Jax


### K
#### Kat
Katalin Zamiar, who portrayed the female ninjas in MKII.

#### Kerri Hoskins
Sonya Blade in MK3.

Also in NBA Jam and Revolution-X.


#### KN
Kano.

#### KT1
Kitana. Or perhaps Katalin 1.
#### KT2
Mileena. May stand for Katalin 2, or Kitana 2. 

### L
#### Lia
Lia Montelongo. Sindel. (She later played Sareena too, but "Lia" in the game files means Sindel.)

#### Liz
Elizabeth Malecki, who portrays Sonya Blade in the first two Mortal Kombat games.


#### LK
- Liu Kang
- Low Kick

### M

#### Michael O'Brien
Stryker in MK3.

#### MOD
Module. Usually "background module", code and data related the backgrounds or stages.

#### Mugs
Character select and ladder portraits. 

#### Murder
Killing (ending) a process. 

### N
#### NJ
Ninja.

#### Nu
New.

#### NUJAX
"New Jax". They refilmed Jax in a new costume. (Old one was yellow.)

#### NUVS
New Vs. As in the new versus screen portraits. 

### O

#### OCHAR
TODO. Something to do with character struct. The "O" prefix is used a lot, but I'm not sure what it means. (Object? Original? Old?)

#### OID
Object Id.

The game maintains lists of objects, and each one has an object id.
Used to locate an object in a list by `id`. 

#### On Deck
[A term borrowed from baseball.](https://en.wikipedia.org/wiki/On-deck). It means "up next", as in who's the next fighter in an endurance match or who's the next fighter in the ladder. In MK1 there's references to `ONDECK_GORO`, which is likely related to special logic in the last endurance match and how the transition to fighting Goro is handled.

#### OSM
Old Smoke. Human Smoke in UMK3.

#### OSZ
Old Sub-Zero. The "Classic" Masked Sub-Zero in UMK3.

#### Otomix

[Otomix](https://www.otomix.com) is a company that makes martial arts and body building gear and clothing. Johnny Cage is wearing their pants in MK2, but the logo was digitally removed in game, except for the soul steal fatality, and for early revisions of the arcade game. The unedited sprites appear in the source leak.

### P

#### Palette
General meaning: A set of colors used in a composition. 

Usually we mean a table of colors associated with a particular image or set of images. Those images use "indexed" color mode.

[GIMP](https://www.gimp.org) makes a distinction between a [palette](https://docs.gimp.org/3.0/en/gimp-concepts-palettes.html) and a [colormap](https://docs.gimp.org/3.0/en/gimp-concepts-palettes.html#idm4763).

#### Pancake
- A fighter collapsing
- A PSX emulator
- Handle of Sergi Alvarez, the author / lead of [radare2](https://github.com/radareorg/radare2) (from which [Rizin](https://github.com/rizinorg/rizin) was forked)

#### PROC
Either "procedure" (another name for "function"), or "process".

The arcade games are written in a multi-process or multi-threaded style.

While the game refers to them as processes, in modern terms we would call them threads, since they share memory.

The game's process switching code requires assembly code, even in the C ports, often in a file with OS (operating system) in its name.

#### prcdsp
Process Display.

A process (proc, thread, task) that handles the display (drawing the screen).

#### prcslp
Process sleep. Puts the current process to sleep for a specified amount of time.


#### PROJ, Projectile
An attack that is a separate object that flies through the air, like a ring toss, sai toss, fan, blade spark, fireball, etc.



### Q
### R
#### Repell
Pushing the players away from each other, and away from the corner, after certain attacks.

#### Richard Divizio
Played Kano in first 3 MK games, as well as Baraka and Kabal. He also did some Raiden sprites for MKT.

#### RLE
Run length encoding.

A simple and fast to decompression method of compressing images.

It's not a single standard, but just a generalized idea with tons of implementations.

The idea is: if you have a bunch of pixels one right after another that are the same color (a "run"), instead of repeating that color over and over again, instead you have a byte that says how many of that color in a row you have, and then the next byte is the color.

If the answer were ever "1", then it would take up more space and not less. So usually there is a scheme to encode bytes literally too. 

It might be something like:
- read a byte
- if it is negative, do RLE logic
  - the "run length" is: (-theByte) + 1
  - read the next byte
  - copy that second byte to the output "run length" times
- if it is positive, the pixel is that byte, copy it to the output

But since you're running in 1990s technology (if you're lucky), you need it to be hyper-optimized. So you'll see hand unrolled loops and things like that. If the CPU reads 4 bytes at a time faster than 1, then you'll see code reading 4 bytes at a time.

Another complication is that your palette is often 64, 32, sometimes even 16 colors. So you don't want to waste space storing all those unused bits. So you end up treating the file as an array of 4, 5, or 6 bits instead of 8 bit bytes, or even as a bit stream. That involves a lot of bit shifting operations, and makes the data harder to see in a hex editor.

#### RD
Raiden.

#### Robo
Robot, Roboninja. Refers to the palette swapped cyber ninjas, Cyrax, Sektor, and Smoke.

Sektor (Ketchup) is usually RB or RB1, with Cyrax (Mustard) being RB2 or ROBO2, and Smoke RB3 or ROBO3.


#### RP
Reptile.

### S
#### SA
"Sword Arms Guy". Baraka.

#### Sal Divita
Played Nightwolf, Sektor, Cyrax, Smoke in MK3.

#### Sans
[Without](https://en.wiktionary.org/wiki/sans).

Sans power is without power.

A "sans-serif" font is "without serifs". (Serifs are the extra tiny lines you find on serif fonts such as Times, but don't see on sans-serif fonts like Arial.)

#### SB
Sonya Blade.

#### SC
Scorpion.

#### SG, She-Goro

Sheeva.

She's often called SG, "She Goro" or sometimes just "Goro" in the MK3 source and assets.

#### Short
Ducking / crouching. `am_i_short` checks if the current process is ducking.

#### Slave
A process created by and controlled by another process, especially as part of an animation.

#### Snot

Semi-solid nasal mucus.

The internal name for Johnny Cage's projectile. Example: `throw_snot` is a function used when the special move is activated.

*You might think it's a booger, but it'snot.*

#### Son of Goro

Kintaro.

Kintaro is not Goro's son in the storyline, but is referred to
as such in the MKII source code and assets. This is often shortened to just "Goro".

#### ST
Shang Tsung.

#### STK
1. Strike
1. Stack

#### Strike, Strike Table

When one player hits another play with an attack. 
The strike table is used to decide when a strike hits, and what happens next.

Usually a **strike** triggers a **reaction**.

#### suicide
Not a in game hara kiri, but instead the name of a function to call for a process
to exit. `murder` is used to end another process, `suicide` to end the current process.

#### SZ
Sub-Zero.

### T
#### Tiger
Kintaro.

#### TMS34010

The CPU used in Mortal Kombat 1, 2, 3 and UMK3.

See https://en.wikipedia.org/wiki/TMS34010 for more information. 

Mame has an emulator for this CPU, see https://github.com/mamedev/mame/blob/master/src/devices/cpu/tms34010/tms34010.h



#### TM
"Tony Marquez". Kung Lao in MKII.

For example, the file `HATHED1.IMG` contains a sprite named `TMSTANCE1`.

#### Trans Rights
Human Rights.

#### TSL
Time Since Last.

Example: `get_tsl` returns the amount of time, in ticks, since the last time the variable in register `a0` was updated.

#### Two's complment
See https://en.wikipedia.org/wiki/Two%27s_complement

It is how negative numbers are stored. Usually.

It means that `-1` is stored as `0xFF`. In binary that is `0b 1111_1111`.

This is useful to know if you are looking at an unknown file in a hex editor. If a field is signed, then `-1` is a common value to use for "N/A" or "not set". 

For example, sprites are often stored as width, height, and x and y offsets, and usually all four of these are each in two byte fields.

Animation offsets are usually small signed numbers, and it's helpful to know that `FF FD` can also mean `-3`.

Neither negative three nor 65,535 (0xFFFD in decimal) are going to be valid sprite widths or heights in a 90s arcade game. But negative three might be a valid x or y animation offset.


### U
#### UG, UGMO
"Ugly Guy". Refers to Baraka.

### V

#### VD
[Van Damme](https://en.wikipedia.org/wiki/Jean-Claude_Van_Damme)

MK1's assets refer to Johnny Cage by this name.

#### VDA
[Truevision TGA](https://en.wikipedia.org/wiki/Truevision_TGA).

> EPICenter's first two cards, the VDA (video display adapter) and ICB (image capture board), used the first incarnations of the TGA file format. The file extensions ".vda" and ".icb" implied information about the board specific data contained.

These files can be opened in some common editors, including GIMP. They're more commonly known by the `.tga` extension.

### W
#### Worldtlx
TODO: better document this.

Related to background scrolling and parallax.

### X
#### XVel
X velocity. How fast a sprite is moving in the X direction (left to right).

### Y
#### Yang Tsung

Yang Tsung is assumed to be an earlier name for Shang Tsung.

This was discovered on November 29th, 2025 by Tim, leanycat and others on Discord.

(That the PC versions contain debugging symbols has been known by the community for quite some time, so it is possible this has been noticed before, but I couldn't find any record of it.)

While going through the list of symbols in the PC (DOS) version of MK1 it was noticed that Shang Tsung's animation frames didn't seem to have symbols. On closer inspection, the symbols were located, but with the prefix `YT`. (As opposed to `EMP`, which is what other Shang Tsung related symbols use.) But none of us could figure out what `YT` might stand for.

At first, Yang Tsung was mentioned as a joke.

But then we noticed that `YTSTANC1` uses a palette named `YANG_P`. (Palettes often end with `_P`.)

#### YT
See *Yang Tsung*.

### Z
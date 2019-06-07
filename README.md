# Ludus-Emu
Another NES emulator written in rust.

This exists as an example of using [the ludus crate](https://crates.io/crates/ludus)
to create a standalone program.

## Installing
Given the few dependencies this app relies on, it should be as simple as:
```
git clone https://github.com/cronokirby/ludus-emu
cd ludus-emu
cargo build --release
```
(Note: you probably want to run on release if you don't want choppy
gameplay.)

## Usage
### Running a game
```
ludus-emu rom
```

By default the largest scaling is chosen, but this can be set manually
as well:
```
ludus-emu rom --scale 2
```

ATM ludus-emu only supports .nes (INES) files, which are the most common
format for nes roms.

## Controls
Right now, only hardwired mapping between keys and controllers is
supported, but in the future I plan to add remappable configuration via
some kind of file format.

| Button | Key |
| :----: | :-: |
| A      | K   |
| B      | J   |
| Start  | H   |
| Select | G   |
| Up     | W   |
| Down   | S   |
| Left   | A   |
| Right  | D   |

In addition, Esc closes the window, and Enter resets the console.

## Current state

### Working
- CPU, and thus core gameplay
- PPU, and thus graphics
- APU, and thus audio
- Basic controls via hardwired key mapping
- Mappers 0, 1, 2, so common games like Super Mario Bros, and Donkey Kong

### Not Working
- Save States of any kind
- Keeping SRAM files for each game
- More complex Mappers

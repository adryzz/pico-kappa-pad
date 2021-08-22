## pico-kappa-pad

A port of the [kappa-pad](https://github.com/EXtremeExploit/KappaPad) for the Pi Pico.

Will have two branches: a key branch and a capacitive touch branch.

The kappa-pad is a capacitive touch keyboard with two keys meant to play [osu!](https://github.com/ppy/osu). 

(Yes, a 4 keys and 7 keys variant is in the works for you mania players.)

## Requirements
* A Raspberry Pi Pico
* 2 330 kOhm Resistors
* Solid core wires
* 2 Pieces of sheet metal

## Setup
* Download the latest release of your choice from the [releases page](https://github.com/adryzz/pico-kappa-pad/releases/latest)
* Plug in your Pi Pico to your PC while holding down the `BOOTSEL` button and copy `pico-kappa-pad.uf2` (or the version of your choice) to the Pico's USB mass storage device.

## Wiring
// TODO: write wiring diagram

### Building

0. Have a working Raspberry Pi Pico C SDK setup.
1. Clone/download the repository. Don't forget to run `git submodule update --init`.
2. Ensure that there is a symbolic link to [`pico_sdk_import.cmake`](https://github.com/raspberrypi/pico-examples/blob/13f89f628258b398ed07cf715ee3432e16e4e76a/pico_sdk_import.cmake) from the Pico C SDK. (If a symbolic link isn't an option, just copy the file.)
3. Create a build directory, `cd` to it, and run `cmake ../`. (Or your build system equivalents.)
4. Build by running `make`. (Or your build system equivalent.)
5. Reset (or plug in) the Pico holding down the `BOOTSEL` and copy `pico-kappa-pad.uf2` to the Pico's USB mass storage device.
6. You should have a keyboard device now. Shorting the pins to ground should press the appropriate keys.

# `i2c-spi-oled-mikrobus-board`

I²C-to-SPI interface board with most mikroBUS pins controllable via I²C.

Combines two chips: SC18IS606PW (I²C-to-SPI) and PCA9557PW (I²C-to-GPIO).

## Addressing

Three bits of the address are chosen through the three jumpers on JP1. The bits are numbered, from
top to bottom, A0, A1, and A2. Bridging the left and middle pins with the jumper sets that bit to 0;
bridging the middle and right pins sets the bit to 1.

Once the jumpers are set, the following addresses are assigned to the chips:

| chip        | MSB | b5 | b4 | b3 | b2 | b1 | LSB | (R/W) |
| ----------- | --- | -- | -- | -- | -- | -- | --- | ----- |
| SC18IS606PW | 0   | 1  | 0  | 1  | A2 | A1 | A0  |       |
| PCA9557PW   | 0   | 0  | 1  | 1  | A2 | A1 | A0  |       |

### Communication

The shuttle board's peripheral select pin is connected to the SC18IS606PW's ¬SS0 pin. Therefore, to
send data via SPI, use function 0x01.

The non-SPI pins are connected to the PCA9557PW as follows:

| PCA9557PW | shuttle board |
| --------- | ------------- |
| P0        | ¬INT          |
| P1        | D/¬C          |
| P2        | EN            |
| P3        | R/¬W          |

Pins P4 through P7 are unconnected.

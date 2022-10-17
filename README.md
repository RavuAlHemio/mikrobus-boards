# mikroBUS Boards

An assortment of boards that should be compatible with [MikroElektronika](https://www.mikroe.com/)'s [mikroBUS standard](https://download.mikroe.com/documents/standards/mikrobus/mikrobus-standard-specification-v200.pdf).

The designs are experimental. They are provided without warranty that the resulting boards will be fit for purpose and without warranty that they will not damage the connected devices.

## Boards

* `i2c-spi-jumper-mikrobus-board`: an I²C-to-SPI interface similar to the [_I2C to SPI Click_](https://www.mikroe.com/i2c-to-spi-click) (MIKROE-3743) and using the same chip ([NXP SC18IS602BIPW/S8HP](https://www.nxp.com/part/SC18IS602BIPW)), but with pin header jumpers instead of re-soldering 0Ω SMD "resistors" to set the I²C address. Perfect for people with no fine motor skills, like myself.

* `i2c-spi-jumper-mikrobus-board-var2`: another I²C-to-SPI interface with jumpers, but using the [NXP SC18IS606PW](https://www.nxp.com/part/SC18IS606PW), since the SC18IS602BIPW/S8HP is end-of-life. A different board is needed because the new chip has a different pinout.

* `i2c-uart-mikrobus-board`: just as the I²C-to-SPI boards allow SPI devices to be controlled via I²C, this board allows UART devices to be contacted via I²C. Based around the [NXP SC16IS740IPW](https://www.nxp.com/part/SC16IS740IPW). To simplify the traces and keep the board a reasonable size, instead of providing a second pair of mikroBUS sockets to connect the UART-enabled device, the design provides a [mikroBUS Shuttle](https://www.mikroe.com/mikrobus-shuttle) pin header. The I²C address is set using rotary switches.

* `knx-mikrobus-board`: a KNX bus coupling unit (BCU) that translates between KNX and UART. Based around the [onsemi NCN5130](https://www.onsemi.com/products/interfaces/wired-transceivers-modems/ncn5130) but should also work with the pin-compatible [onsemi NCN5121](https://www.onsemi.com/products/interfaces/wired-transceivers-modems/ncn5121).

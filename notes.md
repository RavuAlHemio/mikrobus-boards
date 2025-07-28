## mikroBUS Shuttle

The pin header used by MikroElektronika for the mikroBUS Shuttle is a CNC 3221-16-0300-00, available from DigiKey (not Mouser). Most other shrouded pin headers do not have the "open sides" (or only have them at the bottom of the pin header but not near the top).

The canonical pin numbering for IDC connectors is:

1. The key is a protrusion on the connector with sockets (generally on a cable) and a hole on the connector with pins (generally on a device).

2. The row with the key or key-hole is the top row.

3. In the top row, position 1 is the leftmost socket (and, correspondingly, the rightmost pin) when staring at the mating surface of the connector.

4. Position 2 is in the next row right below position 1.

5. Once all rows are exhausted, counting continues at the next position in the top row.

Oddly enough, the Shuttle's ribbon cables are terminated in such a way that pin 1 is top-left on one end of the cable and top-right on the other. This means that the pinout of the Shuttle board (the remote base for a mikroBUS board) is different than that of the Shuttle Click board (the module that plugs into a host board).

Taking all of this into account, the socket pinouts on the boards are as follows, key-hole above the top row.

mikroBUS Shuttle (remote):

|     |       |      |      |      |      |     |     |
| ---:| -----:| ----:| ----:| ----:| ----:| ---:| ---:|
| GND | +3.3V | COPI | CIPO |  SCK |   CS | RST |  AN |
|  15 |    13 |   11 |    9 |    7 |    5 |   3 |   1 |
|  16 |    14 |   12 |   10 |    8 |    6 |   4 |   2 |
| GND |   +5V |  SDA |  SCL | CRPT | CTPR | INT | PWM |

(CRPT and CPTR are the UART pins: Controller Rx/Peripheral Tx and vice versa. The two GND pins are connected together on the Shuttle. The connector is mounted "key-up".)

Shuttle click (base):

|     |     |      |      |      |      |       |     |
| ---:| ---:| ----:| ----:| ----:| ----:| -----:| ---:|
| PWM | INT | CTPR | CRPT |  SCL |  SDA |   +5V | GND |
|  15 |  13 |   11 |    9 |    7 |    5 |     3 |   1 |
|  16 |  14 |   12 |   10 |    8 |    6 |     4 |   2 |
|  AN | RST |   CS |  SCK | CIPO | COPI | +3.3V | GND |

(Here, too, the ground pins are connected internally. The connector is mounted "key-down".)

## ARM SWD debug port

The partially-shrouded 1.27mm pin header used for the ARM SWD debug port is a Samtec FTSH-105-01-F-DV-K-P. The -K specifies the keyed partial shroud and -P specifies a pick & place pad for simplified machine assembly.

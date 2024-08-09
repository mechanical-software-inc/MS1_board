# Design files for MS1 board

## Features
* 6 rp2040 pico's using i2c<->i2c comms for i/o sharing
* 1 rp2040 pico dedicated to ethernet communication (broken on current board, fixing)
* 10x24V Discrete outputs (2 per pico, 5 picos)
* 20x24V Discrete inputs (4 per pico, 5 picos)
* 18x4-20mA inputs (3 per pico, 6 picos) - implemented with rp2040 i/o and external 16-bit i2c ADC - can use without external ADC if needed
* 5x4-20mA outputs (1 per pico, 5 picos)
* 256KB EEPROM with unique 32bit serial number for board ID
* RPi umbilical for pico programming, monitoring, i2c comms

## Images
### Current (block 3)
<p align="center">
  <img src="https://github.com/mechanical-software-inc/MS1_board/blob/main/Images/block3.jpg?raw=true" width="400" title="block 3 image">
</p>

### Past (blocks 1-3)
<p align="center">
  <img src="https://github.com/mechanical-software-inc/MS1_board/blob/main/Images/ms1_blocks1-3.jpg?raw=true" width="400" title="blocks 1,2,3 image">
</p>

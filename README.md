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
* Green is standard spec and cheaper for testing, will probably return to red at some point
* Old style terminal blocks were too small and hard to swap
* Non-resettable fuse was dumb
* Lots of issues with debug pin trace routing and sizing - believe these have been sorted
* Bigger power supply
* On-board ethernet (not working yet, stack is 90%, but pinout is messed up on current board)
* On-board eeprom is new - better than using pico flash chip for ID
* On-board ADC for 4-20mA inputs is new to block 3 - voltage inputs are fed to external ADC and pico inputs for comparison and use when external ADC chips are unobtainium
* Fixed many grounding and power connector issues
<p align="center">
  <img src="https://github.com/mechanical-software-inc/MS1_board/blob/main/Images/ms1_blocks1-3.jpg?raw=true" width="400" title="blocks 1,2,3 image">
</p>

### Software
* Tooling and ethernet stack with Ethernet/IP (industrial protocol) host and MQTT support, still working out bugs, contact for more info

### Limitations
* Board size is not currently a factor for us, we are typically building large control panels
* Will probably create a few different form factors in the future (1-4 picos is easy to see happening)
* i2c comms for inter-board messaging is probably not ideal, but works for us

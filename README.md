## Open Stage Control Trotl Mix
RME's TotalMix Remote controller for dummies

This is a proof-of-concept emulation of RME TotalMix Remote, based on
https://github.com/jean-emmanuel/open-stage-control-mcu
which itself is a proof-of-concept emulation of an MCU with Open Stage Control, based on https://github.com/NicoG60/OscMackieControl.

RME TotalMix Remote is great, packed with bells and whistles, but as a personal monitor controller in a real-world studio session — working with visually impaired drummers, stressed-out singers, and the like — I found it totally unusable. So, this is a stripped-down, bare-bones version designed out of necessity: volume faders with track names, pan knobs (none in the Small version), track/bank selectors, and nothing more.

Open Stage Control Server should run on a Mac or PC with MIDI control enabled in TotalMix Remote. https://openstagecontrol.ammd.net/download/

The Client can run on any device (tablet, smartphone, laptop, etc.) that is on the same network as the Server and has web browsing capabilities.

## Usage

Open Stage Control config:
- `midi: sysex daw:0,1`
    (Replace port numbers if needed. In Open Stage Control, check "List MIDI Devices" — the numbers should correspond to the MIDI Input/Output ports in TotalMix Remote. On a Mac, you can use two IAC Driver MIDI busses.)
Note: The MCU protocol follows screen selection, channel layout, etc., so be sure to set up TotalMix Remote carefully.

- `load`: `path/to/TrotlMix.json` 
	or, for smaller screens 
	`path/to/TrotlMixSmall.json`

- `custom-module`: `path/to/TrotlMix.js`


```

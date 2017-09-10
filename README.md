# PyBdEcho
An audio demonstration using [MicroPython], the [PyBoard] and its [AMP Skin].

For a discussion of the application and its development refer to my
EuroPython [presentation] in Rimini, July 2017.

## Construction
You need good soldering skills to build the [AMP skin].
Once built you'll be able to access the speaker
using DAC port `1` and the microphone's ADC on `X22`.

## Installation
The code's been tested with:
 
*   PyBoard v1.1
*   Audio Skin v1.0
*   MicroPython v1.9.2

>   Remember to _always_ correctly eject the PyBoard from your workstation.
    If you do not you can corrupt the files on Board.

If you need toi update your PyBoard firmware first disconnect it from
your workstation and, if attached, remove the audio skin. You can then
[Update] your PyBoard [firmware] and then re-connect the audio skin before
re-connecting the PyBoard to your workstation.

When connected, the PyBoard should appear as a USB flash device
(probably called `PYBFLASH`).

Copy `main.py` and `PyBdEcho.py`, replacing the files that are there if you
need to, to the root of the device.

Wait for the PyBoard RED LED to extinguish (it takes a few seconds) and then
hit the board's `RST` button.

If all's gone well the RED LED will extinguish after a few seconds
and the GREEN LED should be slowly toggling (with a period of 1.5 seconds).

The toggling LED indicates that the record/playback loop is _on-hold_.
Hitting the `USR` button will pyt the board into _listen_ mode (indicated
by a solid GREEN LED). When the LED is GREEN you should be able to speak
(close to the microphone and, when you've stopped speaking (or exhausted the
recording buffer) the device should playback what it heard.

## Presentation
The presentation slides (exported as a PDF document) can be found in the
`presentation` directory.

### Issue 2
Contains the following minor corrections to the original presentation slides.

-   Typo in first bullet-point of slide `15`. `4096` should be `4095`
-   Correction of the block diagram in slide `23`. The green LED was shown
    as the `Playback` LED when it should have been the blue LED

---

[AMP Skin]:     https://micropython.org/store/#/products/AMPv1_0
[Firmware]:     http://micropython.org/download/
[MicroPython]:  http://micropython.org
[Presentation]: https://ep2017.europython.eu/conference/talks/building-a-real-time-embedded-audio-sampling-application-with-micropython
[PyBoard]:      https://micropython.org/store/#/store
[Update]:       https://github.com/micropython/micropython/wiki/Pyboard-Firmware-Update

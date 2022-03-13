# lumberjack-pcb

this modified lumberjack pcb to hotswap switch (only support cherry switch)
Lumberjack is a split 5x12 ortholinear keyboard PCB using through-hole components only.

Original Repo by the [Lumberjack keyboard](https://github.com/peej/lumberjack-keyboard).

![PCB render front](images/pcb-front.png)

![PCB render back](images/pcb-back.png)

# Ordering parts

See the [Bill of materials](BOM.md) for a detailed list of the required parts.

![BOM](images/bom.jpg)

PCBs can be manufactuered by a variety of online PCB fabricators

The gerber file is ready to produce

[lumberjack.zip](https://github.com/peej/lumberjack-keyboard/blob/master/gerber/lumberjack.zip) PCB.

When uploading the gerber zip files, use the default PCB settings.

![PCB](images/pcb.jpg)

# Construction

Solder all the components onto the top side of the PCB except the USB connector which should be on the back of the board. Leave the larger components until last so that the board will lie flat upsidedown while you solder the resistors and capacitors.

Take care to put the correct value resistors and capacitors in the correct places, the values are written on the silkmask along with the component reference. If you are unsure about the value of a resistor, check it with a multimeter.

Ensure that polarised components (diodes, LEDs, electrolytic capacitor (C3), IC socket) are in the correct orientation. The square pad is for the negative side of the component; for a diode this means the side with the black stripe; for LEDs and C3 the short leg is the cathode and goes in the square pad.

See [the build guide](guide.md) for more information.

# Firmware

Firmware is available in the QMK repository under the name `peej/lumberjack`.

Follow the [QMK firmware instructions](https://beta.docs.qmk.fm/using-qmk/guides/flashing/flashing) to build and flash the firmware.

To put the board into bootloader mode so it is ready to recieve firmware, press and hold the BOOT button (SW2) while pressing and releasing the RESET button (SW1). The board will now be detected as an USBasp device and can have the firmware flashed via the USB port.

Pressing the RESET button (SW1) on its own will restart the microprocessor. Once flashed with firmware it is neccessary to reset the keyboard so as to return control to the new firmware.

Note that due to the BOOT button (SW2) sharing a pin with column 3, when pressed the keys in that column will also activate. This is expected behavour but can be a little annoying or confusing if you are not expecting it.

# Revisions

## Rev 1.6 cherry

- change to hotswap switch universal ( cherry only )

# EV Throttle Potentiometer

A potentiometer part I designed in Fusion 360 for the Lafayette EV Club's electric race car. It's the piece of the throttle pedal that tells the car how much power the driver wants.

![Potentiometer model](potentiometer.png)

## How it works

The pedal turns the potentiometer's shaft. As the shaft turns, the potentiometer's resistance changes, so the signal it sends back changes too. That signal is how the car knows how far the pedal is pressed. It was used to find power supplied to the system by the driver's leg, in percentage.

## What's in the model

- A base plate with a rotary potentiometer
- A connector for the wiring
- A mounting hole

## Gearbox assembly

![Gearbox assembly](gearbox-assembly.png)

The gearbox in the same project, modeled as a full assembly in Fusion 360:

- Housing
- Brass gear on a brass gear shaft
- Plastic gear on a plastic gear shaft
- Flywheel
- Oil-embedded bronze sleeve bearings
- Retaining rings, a Woodruff key, and stainless steel screws (off-the-shelf McMaster-Carr parts)

## Circuit (KiCad)

![KiCad schematic](schematic.png)

Parts in the schematic:

| Ref | Part |
| --- | --- |
| Q1 | 2N7000 N-channel MOSFET |
| BZ1 | Buzzer |
| R1 | 10 MΩ resistor |
| C1 | 1 nF capacitor |
| J1 | DC jack |
| J2 | 2-pin screw terminal |
| Z1 / Z2 | 12 V supply / 9 V battery |

Here's how it works. The buzzer sits between VCC and the MOSFET. R1 holds the MOSFET's gate low, so the buzzer stays off. When the two screw-terminal pins get connected, the gate is pulled up to VCC, the MOSFET turns on, and the buzzer sounds. C1 filters noise on the gate.


## Files

| File | What it is |
| --- | --- |
| `potentiometer1.stl` | 3D model of the potentiometer part. Click it on GitHub to spin it around. |
| `potentiometer.png` | Render of the potentiometer part |
| `gearbox-assembly.png` | Fusion 360 screenshot of the gearbox |
| `schematic.png` | KiCad schematic |

## Tools

Fusion 360, KiCad

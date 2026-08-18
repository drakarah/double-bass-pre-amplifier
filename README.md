
# Double bass pre-amplifier

A pre-amplifier for a double bass pickup that requires high impedance on the input side.

## Why 

Commercial options are very expensive, I wanted to make a DIY version for much cheaper and learn about analog electronics (completely new to me).

Cheaper bass pre-amplifiers don't have enough impedance on the input and thus loses a lot of the lower frequencies from the pickup.

## How it works

2 OPA2134 op amps that work with 5 stages:

1. Buffer: separate the high impedance requirement from the rest of the circuitry
2. High pass filter: reduce anything lower than ~28Hz to get rid of contact noise.
3. Gain: boost the voltage according to a gain factor, 0 -> 3x
4. Treble: boost or reduce the treble
5. Bass: boost or reduce the bass

Everything is powered with a 600mA lipo battery, usb charge board and XL6009 boost converter to get 9V. Higher voltage provides more headroom for larger amplification but uses more current (a hard pluck can get up to 600mV on the input)

Contains:

- Schematic in [LTSpice](https://www.analog.com/en/resources/design-tools-and-calculators/ltspice-simulator.html) for running simulations
- Perf board layout in [DIY layout creator](https://github.com/bancika/diy-layout-creator)
- FreeCAD case design

## BOM

## Bill of Materials

### Power circuitry

| Reference(s) | Value / Description | Qty |
|---|---|---:|
| LatchingPowerSwitch | Latching power switch | 1 |
| LED_POWER | LED | 1 |
| Lipo batt | Battery | 1 |
| — | OPA2134 Op-amp | 2 |
| — | 8-PIN DIP SOCKET | 2 |
| — | USB charge board | 1 |
| — | XL6009 | 1 |
| — | USB-C connector | 1 |

### Amplifier

| Reference(s) | Value / Description | Qty |
|---|---|---:|
| Perf Board w/ Pads | | 1 |
| Cbass, Cdec_HF, Cdec_HF2, Chpf | 100 nF 50 V, Ceramic | 4 |
| Cbias, Cdec_LF | 10 µF 50 V, Electrolytic | 2 |
| Cin | 100 nF 63 V, Ceramic | 1 |
| Cout | 1 µF 63 V, Film | 1 |
| Ctreble | 47 nF 50 V, Ceramic | 1 |
| D1, D2 | 1N4148 diode | 2 |
| Input jack, Output jack | Audio jack | 2 |
| Rbass_fb, Rbass_in, Rgain, Rled | 4.7 kΩ | 4 |
| Rbias_bottom, Rbias_top, Rout_pulld | 100 kΩ | 3 |
| Rhpf_bias | 56 kΩ | 1 |
| Rin | 10 MΩ | 1 |
| RoutIso | 100 Ω | 1 |
| RpotBass, RpotGain, RpotTreble | 10 kΩ Linear potentiometer | 3 |
| Rprot | 1 kΩ | 1 |
| Rtreble_fb, Rtreble_in | 10 kΩ | 2 |
| Rtreble_s1, Rtreble_s2 | 2.2 kΩ | 2 |

### Case

| Reference(s) | Value / Description | Qty |
|---|---|---:|
| — | Filament for 3D-printed case | — |
| — | M3 3×5×4 heat-set inserts | 10 |
| — | Copper tape for creating a Faraday cage | ~2 m |
| — | M3×6 mm bolts | 10 |
| — | Velt sheets to protect the double bass from scratches | 1 |




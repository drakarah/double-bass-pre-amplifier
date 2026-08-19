
# Double bass pre-amplifier

A pre-amplifier for a double bass pickup that requires high impedance on the input side.

<img width="719" height="1141" alt="image" src="https://github.com/user-attachments/assets/102a4544-d3b2-4bca-897c-e69831a33c9c" />

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
| LatchingPowerSwitch | [Latching power switch](https://nl.aliexpress.com/item/1005010256927158.html) <img width="143" height="147" alt="image" src="https://github.com/user-attachments/assets/3b7811c6-25ee-4b0f-bc77-410cd06c594c" />
 | 1 |
| LED_POWER | LED | 1 |
| Lipo batt | Battery | 1 |
| — | OPA2134PA Op-amp | 2 |
| — | 8-PIN DIP SOCKET | 2 |
| — | USB charge board | 1 |
| — | XL6009 | 1 |
| — | [USB-C connector](https://nl.aliexpress.com/item/1005009250540441.html) <img width="168" height="128" alt="image" src="https://github.com/user-attachments/assets/f760b4a2-6215-4e29-91d1-c1ea47e37ea8" /> | 1 |
| — | JST connector male | 1 |

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
| Input jack, Output jack | 6.3mm Audio jack | 2 |
| Rbass_fb, Rbass_in, Rgain, Rled | 4.7 kΩ | 4 |
| Rbias_bottom, Rbias_top, Rout_pulld | 100 kΩ | 3 |
| Rhpf_bias | 56 kΩ | 1 |
| Rin | 10 MΩ | 1 |
| RoutIso | 100 Ω | 1 |
| RpotBass, RpotGain, RpotTreble | 10 kΩ Linear potentiometer | 3 |
| Rprot | 1 kΩ | 1 |
| Rtreble_fb, Rtreble_in | 10 kΩ | 2 |
| Rtreble_s1, Rtreble_s2 | 2.2 kΩ | 2 |
| — | JST connector female | 1 |
| — | Preferably shielded cable for the input (e.g an old good USB cable) | 1 |

### Case

| Reference(s) | Value / Description | Qty |
|---|---|---:|
| — | Filament for 3D-printed case | — |
| — | M3 3×5×4 heat-set inserts | 10 |
| — | Copper tape for creating a Faraday cage | ~2 m |
| — | Kapton tape to prevent short circuits | 1 |
| — | Double sided tape to hold power electronics in place | 1 |
| — | M3×6 mm bolts | 10 |
| — | Velt sheets to protect the double bass from scratches | 1 |
| — | 4mm standoffs so wires clear the perf board better | 4 |
| — | Ring terminal for connecting lid and case shielding together | 2 |
| — | Washer to apply pressure onto the shield | 2 |

### Misc

| Reference(s) | Value / Description | Qty |
|---|---|---:|
| — | Plenty of wiring | — |
| — | Heat shrink to prevent short circuiting VCC to the copper tape | — |


## Pictures

<img width="993" height="513" alt="image" src="https://github.com/user-attachments/assets/0e689048-48a6-4af6-b755-2d1cc94d24d3" />

<img width="952" height="530" alt="image" src="https://github.com/user-attachments/assets/0ec683e6-e297-4175-b46f-3f1a10303d13" />

<img width="983" height="551" alt="image" src="https://github.com/user-attachments/assets/0bda1509-3ff7-428c-bbef-a7fd5b4e7d7c" />

<img width="982" height="961" alt="image" src="https://github.com/user-attachments/assets/075c554b-cf3e-4a47-9890-2e7bf32520a4" />

<img width="988" height="1058" alt="image" src="https://github.com/user-attachments/assets/9baf2ea2-cf0f-4f55-9cfa-4e6e755d8968" />

<img width="984" height="891" alt="image" src="https://github.com/user-attachments/assets/950a8638-12b7-47b3-90e1-ac9be4677926" />

<img width="975" height="638" alt="image" src="https://github.com/user-attachments/assets/2f391ca6-2afe-48fa-9e03-3bd14653e84c" />


<img width="869" height="863" alt="image" src="https://github.com/user-attachments/assets/4dde837d-4f35-43b6-911c-23079dfbdb2f" />

<img width="616" height="613" alt="image" src="https://github.com/user-attachments/assets/e1b74b59-79bf-44b8-ba60-e70a9a6e96c0" />

<img width="924" height="781" alt="image" src="https://github.com/user-attachments/assets/3da506ad-f0ac-484a-b9de-77bbe3037ed0" />

## Remarks

Building should be fairly straight forward. 

Solder the negative lead of the LED to the shield to ground the shield.

Set XL6009 to 9V. Higher works too if you want more headroom (if your components allow for it) but it drains the battery faster.

I seperated vcc, vbias Jumper wires to the top of the board, while signal wiring is done at the bottom of the board so they don't interfere and inject noise.

I used male Dupont pins to make my life easier for soldering wires to as well give me some test locations to verify the circuit is working.

I used an oscilloscope with a signal generator attached to the input to check the output of the various stages and whether they behave as expected.

I also played back a sine sweep and recorded both input and output with audacity to check the frequency response is as it is in LTSpice.

I used super glue to glue the components in place.

In the pictures I have too many resistors on the input side that I bridges, disregard those, I initially had gain -> buffer and that did not work well, had a lot of distortion and instead of starting from scratch I modified the existing circuit.

In the pictures I also have hexagons instead of octagon holes in the case, that's because I can't count apparently and didn't notice until after fitment, I updated the case model to use octagons with a bit of tolerance now.



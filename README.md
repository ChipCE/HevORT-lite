# HevORT lite doc (work in progress)

Lower cost, trim down version of [MirageC79's HevORT](https://github.com/MirageC79/HevORT) corexy design. I was designing this machine to be a lowcost and fast machine for parts prototyping, but it ended up the best machine in my small farm, thank to hevort solid XY axis and small size frame.

![front-view](https://github.com/ChipCE/HevORT-lite/blob/master/img/front.jpg)
![side-view](https://github.com/ChipCE/HevORT-lite/blob/master/img/side.jpg)

## About the next release

I'm working on the next of this machine.

- HevORT-like 3 points mounting bed and belted Z instead of ballscrews.
- Dragon hotend toolhead.
- Brush for nozzle cleaning.
- Circular air filter.
- Hevav-like cooling.(I'm not sure if we really need this, since other material than PLA doesn't need much that cooling.)
- Filament spool holder inside the machine chamber.

## About this project

- Small printer that stable and can print fast
- Use off-the-shell parts
- Does not need special tool to make the parts
- Affordable price
- Semi enclosed by default, can be convert to fullly enclosed if needed.If you want fully enclosed frame, get the 4 main vertical extrusion about 150mm longer

## Feature

- Total cost under $500
- Can do the speed benchy for under 12 mins
- Max acceleration 7500mm/s^2 without losing printing quality(tested with klipper ringing tower calibration)
- "Quality" cura print profile at base speed 300mm/s, 60-100mm/s wall, 150mm/s top-bottom layer, 5000 mm/s^2 accel
- Pre-config klipper firmware for SKR1.4
- Intergrated PSU control with sonoff-tasmota
- Optional top-hat(comming soon)
- Chamber thermistor and controllable case light
- Can use any HevORT compatible extruder (standard and HT XY axis).

## Limitations

- To make the printer small using any other extruder than the default option (Mini sherpa + mosquitto) my result in losing build volume
- The design is made for NIC autotech ASF frame(Misumi selling), Other type of 3030 frame can be used without or mirror modify
- No build manual yet, I don't have plan to make it yet. Support only availabe via chat or mail.

## Q/A

- Why only 2 lead screw instead of 3?  
  <code>The bed is small(180x180mm) so even a single leadscrew will be fine. But the board have extra port for the second Z so I decided to go with 2 Z.</code>

- Why using the prusa mini bed?  
  <code>The price is resonable(clone), easy to mount and does not require custom cut aluminum plate.</code>
- Why the bed carrier is too complex, that will also raise the cost?  
  <code>I over did it, it can be more simple. On other hand, the prusa bed carrier have mounting holes on the corners, but just a single mount point is not enough to keep the bushing mounter from tilting. The CF rods were use to keep the mounter from tilting. 5mm CF rods is are cheap and widely available.</code>
- Why use the non standard ASF frame?  
  <code>They are the only thing I can get in my location. Misumi selling them too, so I dont think that will be problem.</code>
- Single 5015 for layer fan is underpower, why don't use berdair?  
  <code>First,there is no space to mount the pump. Second, a good single 5015 is fine. I only need 75% fan with PLA, other type of filament even need less. I only need more cooling when do the speed benchy run, but that's not the speed for printing quality parts. Too strong cooling also push the overhang down before the fan have enough time to cool it down.</code>

## BOM

comming soon

## In development

- Newer version with Wobble wings like mechanism or belted Z instead of lead screw.
- Physic button power control for pi and sonoff-psu

## Thing might change

- The extruder cable mounter. I'm thinking to change this part to make the printer easier to fully enclosed.

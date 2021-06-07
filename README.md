# HevORT lite doc (work in progress)

Lower cost, trim down version of [MirageC79's HevORT](https://github.com/MirageC79/HevORT) corexy design. I was designing this machine to be a lowcost and fast machine for parts prototyping, but it ended up the best machine in my small farm, thank to hevort solid XY axis and small size frame. You can see it in action on [youtube](https://youtu.be/qDmU6JHQ-gc)

![front-view](https://github.com/ChipCE/HevORT-lite/blob/master/img/front.jpg)
![side-view](https://github.com/ChipCE/HevORT-lite/blob/master/img/side.jpg)

## About the next release

While trying to make upgrade for the next release, I ended up with redesign all of the parts. Since there is no Original HevORT parts on the build, the next release will be released under other name. Futher release available [SnakeOilXY repo](https://github.com/ChipCE/SnakeOil-XY)

I'm working on the next upgrades of this machine. For in-development update, feature request or sugguestion, contact me on [twitter](https://twitter.com/ChipMaple).  
Work in progress files are available [here](https://github.com/ChipCE/SnakeOil-XY)

- Redesign XY axis to make it printable without support. Move AB motor into inside to make the machine easier to enclosure(optional).
- Auto detec and load bed mesh profile based on flex sheet.
- HevORT-like 3 points mounting bed and belted Z instead of ballscrews.
- Dragon hotend toolhead with mgn12 and mgn9 support.
- Brush for nozzle cleaning.
- Circular air filter.
- Hevac-like cooling.(I'm not sure if we really need this, since other material than PLA doesn't need that much cooling.)
- Filament spool holder inside the machine chamber(optional).
- Adapt for other type of 3030 frame.
- Carbon fiber X gantry mounter and 2010 extrusion gantry mounter.  

## About this project

- Small printer that stable and can print fast
- Use off-the-shell parts
- Does not need special tool to make the parts
- Affordable price
- Semi enclosed by default, can be convert to fullly enclosed if needed.If you want fully enclosed frame, get the 4 main vertical extrusion about 100mm longer

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
  Edit: 3 points bel leveling and belt driven Z will be added on the next release.  

- Why using the prusa mini bed?  
  <code>The price is resonable(clone), easy to mount and does not require custom cut aluminum plate.</code>  
  Edit: Next release will have option for alumium bed.  
  
- Why the bed carrier is too complex, that will also raise the cost?  
  <code>I over did it, it can be more simple. On other hand, the prusa bed carrier have mounting holes on the corners, but just a single mount point is not enough to keep the bushing mounter from tilting. The CF rods were use to keep the mounter from tilting. 5mm CF rods is are cheap and widely available.</code>  
  Edit: Custom aluminum bed and 2020 bed carrier will be added on the next release.
  
- Why use the non standard ASF frame?  
  <code>They are the only thing I can get in my location. Misumi selling them too, so I dont think that will be problem.</code>  
  Edit: I'm working on support for other types of 3030 frame.
  
- Single 5015 for layer fan is underpower, why don't use berdair?  
  <code>First,there is no space to mount the pump. Second, a good single 5015 is fine. I only need 75% fan with PLA, other type of filament even need less. I only need more cooling when do the speed benchy run, but that's not the speed for printing quality parts. Too strong cooling also push the overhang down before the fan have enough time to cool it down.</code>

## BOM
Not available yet.

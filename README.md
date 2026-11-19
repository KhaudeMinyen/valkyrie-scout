# valkyrie-scout
An SAR fixed wing drone. Designed to be open-source, cheap, and reliable.

A twin-boom pusher fixed-wing for search and rescue, built from XPS foam, carbon tube and printed PETG-CF, and flown with ArduPlane. This README is a plain-text summary so the design can be read at a glance on GitHub. The interactive 3D model and the full bill of materials live in the HTML files listed at the bottom: download one and open it in a browser.

*Design revision 1.8 (3D model) · BOM revision 1.97 · November 2026*

## At a glance

| | |
|---|---|
| Wingspan | 1400 mm (630 + 140 fuselage + 630) |
| Overall length | 920 mm |
| Wing | NACA 2412, 280 mm chord, 0.39 m², aspect ratio 5.0 |
| Wing loading | about 34 g/dm² at 1.35 kg |
| Fuselage | 700 × 140 × 120 mm, 10 mm XPS walls (120 mm wide inside) |
| Booms | Ø10 mm CF tube, 640 mm long, 325 mm apart |
| Tail | NACA 0012, 160 mm chord × 500 mm span, tail volume 0.38 |
| Elevator | one 309 × 64 mm panel between the fins |
| Fins | NACA 0009, 100 × 120 mm, rudders 35 mm deep |
| Motor and prop | Sunnysky X2212 980 kV, direct drive, 10×4.7 pusher (Ø254 mm) |
| Prop height | centre 150 mm above the belly, tips 23 mm above it, 22 mm ahead of the tail |
| Centre of gravity | 70–84 mm behind the wing leading edge (25–30% of chord) |

## Layout (to scale: 1 column = 20 mm, 1 row = 40 mm)

Top view, nose up. `#` marks the booms and the spine fairing; the wing is the wide box.

```
                                 ___
                                /     \
                                |     |
                                |     |
                                |     |
+-------------------------------+-----+-------------------------------+
|                               |     |                               |
|                          #    |     |    #                          |
|                          #    |     |    #                          |
|                          #    |     |    #                          |
|                          #    |     |    #                          |
|                          #    |  #  |    #                          |
+--------------------------#----+--#--+----#--------------------------+
                           #    |  #  |    #
                           #    |  #  |    #
                           #    |  #  |    #
                           #    |  #  |    #
                           #    -------    #
                           #(~~~~~~~~~~~~~)#
                      +-------------------------+
                      |    #               #    |
                      |    #...............#    |
                      |    #    ELEV       #    |
                      +-------------------------+
```

Side view, nose left. The prop is the vertical bar behind the motor `M`.

```
                                     |      ||
                                     |      ||
                                #### |      ||
          ===============###########M|------||-
.-------------=======================|=========
|                                  | |
|                                  | |
'----------------------------------+
```

## How it goes together

- **Wing:** two separate 630 mm XPS foam panels, joined at the fuselage. Ailerons are 300 × 70 mm. The wing leading edge sits 210 mm back from the nose.
- **Spars:** four carbon pieces cut from 1 m stock, 695 mm each. Per wing, one Ø10 tube at 28% chord and one Ø6 rod at 68% chord. Each runs 630 mm in the wing and 65 mm into the holder, and is glued into its wing. A 10 mm stopper in the middle of the holder splits the two sockets 65 mm + 65 mm.
- **Wing mount:** a printed holder on the fuselage roof: wing attachment plate, fuselage roof and backplate, bolted through with M4 heat-set inserts.
- **Wing retention (planned):** magnets. Each wing root has a 100 × 20 × 5 mm printed plate recessed into the foam with two bars, and the holder block has two matching bars on each side face. The tubes carry the lift and the magnets only stop the wing sliding out.
- **Motor:** mounted on a printed spine fairing epoxied to the fuselage roof. The spine starts 450 mm behind the nose, is 40 mm wide with a 2.4 mm base flange, and rises about 50 mm to the motor mount plate at the end of the fuselage.
- **Tail:** twin Ø10 CF booms, one elevator panel between the fins with a servo at each end, rudder servos outboard of the booms.
- **Electronics:** 4S 5200 mAh battery forward, flight controller aft of it, GPS under the roof hatch, ESC near the rear. Placement is illustrative until the first balance check.
- **Printing:** PETG-CF through a 0.6 mm hardened nozzle.

## Open issues

- The wing holder file (`parts/WingFuselageV2-Holder.3mf`) has no tube sockets: both plates are 163 × 140 × 8 mm with two Ø5.5 holes each, both on one side and 11 mm from a tube axis. The sockets need a block on top of the plate, about 28 mm tall.
- The backplate is 140 mm wide and the fuselage is only 120 mm wide inside. Trim it to about 118 mm or notch the walls.
- The magnet joint is untested. Measure the pull on a luggage scale (aim for at least 2 kg per wing) and keep the compass at least 15 cm from the nearest magnet. Use a high-temperature grade (N42SH) if the plane will sit in a hot car.
- In the 3D model the battery (138 mm long) overlaps the solid 90 mm nose block by about 19 mm. Slide the battery back or hollow the nose.
- Placeholders in the drawing: aileron, elevator and rudder sizes, the hatch outline, the spine shape, motor can and prop adapter lengths, and the electronics positions.

## Bill of materials, phase 1 (flight-ready fixed wing)

**Grand total: $829.** Prices are the unit prices in `bom/fw-bom.html` and are estimates.

**Airframe** — $175

| Qty | Part | Unit | Ext | Source |
|---|---|---|---|---|
| 1 | XPS Foam Sheet 2″ × 4′ × 8′ | $17 | $17 | Home Depot |
| 1 | XPS Foam Sheet 1″ × 4′ × 8′ | $12 | $12 | Home Depot |
| 2 m | Ultracote Fluorescent Orange (HANU895) | $14/m | $28 | Horizon Hobby |
| 0.5 m | Ultracote White (HANU870) — trim only | $10/m | $5 | Horizon Hobby |
| 2 | Carbon Fiber Tube 10 mm OD × 8 mm ID × 1 m (booms) | $11.50 | $23 | ReadyMadeRC |
| 2 | Carbon Fiber Tube 10 mm OD × 8 mm ID × 1 m (main wing spars) | $11.50 | $23 | ReadyMadeRC |
| 2 | Carbon Fiber Rod 6 mm OD × 1 m (anti-rotation spars) | $9 | $18 | ReadyMadeRC |
| 1 | BSI Foam-Cure CA Glue | $8 | $8 | Amazon |
| 1 | BSI Insta-Set CA Accelerator | $6 | $6 | Amazon |
| 1 | BSI Slow-Cure 30-min Epoxy (BSI-205, 4.5 oz) | $15 | $15 | Amazon |
| 1 | J-B Weld ClearWeld 5-Minute Epoxy Syringe (25 mL) | $8.49 | $8 | Tractor Supply |
| 1 kit | Hot-Wire Bow Kit (DIY) | $12 | $12 | Amazon |

**Electronics** — $441

| Qty | Part | Unit | Ext | Source |
|---|---|---|---|---|
| 1 | SpeedyBee F405 WING APP Flight Controller | $48 | $48 | RaceDayQuads |
| 1 | Skystars Uranus F4 BLHeli_32 35A ESC (3–6S) | $18.99 | $19 | Pyrodrone |
| 1 | Sunnysky X2212 V3 980KV Brushless Motor | $20.99 | $21 | ReadyMadeRC |
| 6 (8-pack) | MG90S 9g Digital Metal Gear Servo (8-pack, 2 spares) | $3 | $24 | Amazon |
| 1 | Matek SAM-M10Q-5883 GNSS Module | $40.99 | $41 | RaceDayQuads |
| 1 | RadioMaster ER6 ELRS 2.4 GHz PWM Receiver | $29.99 | $30 | RaceDayQuads |
| 1 | RadioMaster Pocket ELRS 2.4 GHz Transmitter | $95.99 | $96 | Pyrodrone |
| 1 pair | MicoAir LR24-F 2.4 GHz LoRa Telemetry Radio (air + ground) | $58.99 | $59 | Pyrodrone |
| 1 | Remote ID Module (FAA-required) | $30 | $30 | Dronetag |
| 1 | Pitot Tube Airspeed Sensor (Matek ASPD-7002) | $18 | $18 | GetFPV |
| 1 | RunCam Thumb Pro (or similar nano cam) | $55 | $55 | GetFPV |

**Power** — $107

| Qty | Part | Unit | Ext | Source |
|---|---|---|---|---|
| 1 | Tattu 4S 5200 mAh 35C LiPo — XT60 | $55.99 | $56 | Pyrodrone |
| 2 | XT60 Connector Pair (M + F) | $3 | $6 | Amazon |
| 1 | 14 AWG Silicone Wire (1 m red + 1 m black) | $10 | $10 | Amazon |
| 1 | iSDT Q6 Retro LiPo Charger | $35 | $35 | GetFPV |

**Printed parts** — $8

| Qty | Part | Unit | Ext | Source |
|---|---|---|---|---|
| ~250 g | Polymaker PETG-CF Filament (1 kg spool) | $30/kg | $8 | Polymaker |

**Hardware** — $98

| Qty | Part | Unit | Ext | Source |
|---|---|---|---|---|
| 1 bag | M3 Hex-Head Screws Assorted (20 mm / 12 mm / 8 mm) | $8 | $8 | Amazon |
| 20 | M3 × 5 mm Brass Heat-Set Inserts (100 pack) | $6 | $6 | Amazon |
| 1 bag | Nylon Control Rods + Z-Bend Clevis Kit | $4 | $4 | Hobby shop |
| 4 | Servo Extension Lead 15 cm JR (female–female) | $1 | $4 | Amazon |
| 1 | Propeller 10 × 4.7 SF (slow-fly, pair) | $6 | $6 | Hobby shop |
| 1 bag | 2.54 mm Dupont Pre-Crimped Wire 15 cm | $4 | $4 | Amazon |
| 1 | LiPo Fireproof Battery Bag | $8 | $8 | Amazon |
| 1 pack | Servo Horn / Arm Variety Pack (25-tooth) | $4 | $4 | Amazon |
| 1 | Magnetic Prop Balancer | $8 | $8 | Amazon |
| 1 | Battery Voltage Alarm (LiPo Buzzer) | $3 | $3 | Amazon |
| 8 | Neodymium Block Magnet 1 × ½ × ⅛ in, N42SH (K&J BX082SH) | $4.10 | $33 | K&J Magnetics |
| 1 bag | M2 / M4 Heat-Set Inserts + Hex Screws Assortment | $10 | $10 | Amazon |

Notes:

- The radio transmitter is a RadioMaster Pocket ELRS in this list ($96). Skip it if you already own an ELRS transmitter.
- The charger ($35) and the camera ($55) are optional. Remove them for a basic build.
- Printer requirements are not in the total: PETG-CF needs a hardened steel nozzle and an all-metal hotend. On an AnkerMake M5 that is the all-metal hotend set plus a 0.6 mm hardened steel nozzle.
- Hot-wire bow: build it from scrap wood and nichrome if you have the materials.
- The PETG-CF cost is pro-rated from $30/kg for about 250 g.
- ArduPlane and Mission Planner are free.

Phase 2, a QuadPlane VTOL add-on, would add about $165 (four lift motors and ESCs, props, outrigger brackets, and a 6S battery).

### Prices to confirm before ordering

- The iSDT Q6 Retro charger ($35) comes from earlier research and has not been rechecked.
- The M2/M4 heat-set insert and hex screw assortment ($10) is an estimate.
- The magnet bars ($4.10 each) and the epoxy ($8.49) were checked on the K&J Magnetics and Tractor Supply sites; stock was not confirmed.

## Files

| Path | What it is |
|---|---|
| `3d-model/sar-3d.html` | Interactive 3D model with toggleable dimensions (download and open in a browser) |
| `bom/fw-bom.html` | Full BOM with notes and a category filter |
| `blueprint/blueprint.html` | Original 2D blueprint, Rev 1.1 (out of date; the 3D model is current) |
| `parts/WingFuselageV2-Holder.3mf` | Wing holder plates |
| `printing/dry_filament_8h.gcode` | Dries filament on the AnkerMake M5 bed for 8 hours |

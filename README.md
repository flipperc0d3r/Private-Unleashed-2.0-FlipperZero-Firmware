### Private-Unleashed-v2.0-for-FlipperZero ###
Rolling Code Exploitation &amp; Relay Attacks

Records legitimate key fob transmissions
Analyzes the sequence to predict future unlock codes
Injects those codes to gain unauthorized access
In effect, attackers “learn” the combination to the digital lock after observing it in use.

Captures and extends the car’s “key nearby” signal
Relays it to the actual key inside a home or office
Sends the legitimate key’s reply back to the car
The vehicle unlocks and starts, believing the key is present

This will not allow you to start or drive away with a vehicle

⚠ Warning ⚠

This firmware is intended solely for experimental and educational purposes on vehicles that you own and is not meant for any illegal activities. I will also not be responsible if you brick your key fob. Additionally even though its almost next to impossible to brick your flipper if you manage to do so again no responsible.

⚠ Warning ⚠

This assumes you are already running unleashed-firmware 080+

I highly suggest you use the flipper build tool to flash to the updated firmware however feel free to use qflipper if you find you're not savvy enough.


**** Additional Notes ***

Modulation: Most of Kia, Hyundai, Mitsubishi and Suzuki factory systems are using FM476 (in
rare cases older models before 2014 are using AM650). Volkswagen, Skoda, Seat, Audi, Ford
ASK, Subaru & FCA are only AM650, additional alarms in most cases are also AM650, some of
aftermarket alarms like Scher-Khan could be FM238 or FM476. Barriers all are AM650 (there is
few exceptions with FM476/custom FSK, in development). For PSA FM need to use custom
presets (in development).

Usage of captured signal: it’s better to save a signal first instead of instantly emulating it from
receiver info menu. Emulation from RX is also working with counter increment, but just the
received command. In order to use all buttons (lock / unlock / trunk / panic / etc. – in case of
vehicles; and additional objects – in case of multi-button garage remotes) and guarantee
proper emulation - use signal from already saved! Always hold emulation button (center or
arrow) at least for 2 seconds (for some protocols need to hold even longer) to ensure all data
passed over-the-air. Center button is always a received command, arrows is other commands.
For example: if we received close / lock command then our center button is always close / lock,
arrow up is open / unlock, arrow down is trunk.

How to copy FAAC SLH / BFT: this kind of remotes requires seed and counter values
calculation. In order to create working clones need to read from each button of each remote at
least 2 consecutive presses without gaps and send me screenshots from receiver info (where is
all details shown: key, fix, hop, etc.). Then I can calculate all data for Sub-GHz Add Manually.

*** 1 December 2025 ***
+ Added support for old Audi models;
+ Improved CC1101 drivers, HAL and Sub-GHz worker module - no more freezes / crashes with custom high-speed presets, faster PSA brute-force;
+ New super-easy and fast update procedure via just 1 .tgz file in automatic mode (saves time and MCU write resource);
+ Improved stability of private protocols work;
+ Added updates from OFW and public Unleashed;

*** COMING SOON Under current development ***
+ New Ford, Land Rover, Jaguar, Lincoln, Mercury FSK & Keyless-Go up to 2023
+ BMW and Mini Cooper
+ Honda
+ Mazda

*** As of November 2025 Current Supported Models ***

✅ KIA MOTORS (UP TO 2025 MODELS)
| Forte | Magentis | Sedona |
| Rio | Mohave | Sorento |
| Rio X-Line | Optima | Soul |
| Carnival | Picanto | Sportage |
| Cerato | Ceed | Stonic |
| Cerato Coupe | Ceed JD | Venga |
| Bongo |

✅ HYUNDAI (UP TO 2025 MODELS)
| Accent | HB20 | i35 | Solaris |
| Avante | H1 | i40 | Sonata |
| Creta | i10 | iMax | Starex |
| Elantra | i20 | iLoad | Trajet |
| Getz | i25 | iX20 | Tucson |
| KRX 2025 | i30 | iX25 | Veloster |
| Mistra | i35 | iX30 | Verna |
| Sante-Fe | iX35 | iX40 |
| iX45 |

✅ SUBARU
| B9 Tribeca | Legacy | XV |
| Forester | Outback |
| Impreza |

✅ Land Rover (UP TO 2016 MODELS)

✅ FIAT (UP TO 2012 MODELS)
| Cronos | Doblo |
| Ducato |

✅ LANCIA
| Delta | Momo |
| Ypsilon | other FCA |

✅ FORD (UP TO 2016 MODELS)
| B-Max | Flex | Ranger | Transit |
| C-Max | F150–F450 | S-Max | Transit Connect / Custom |
| Edge | Fusion | Taurus | Tourneo Connect / Custom |
| Escape | Galaxy | Transit | Grand |
| Escort | Kuga | Transit Custom | Fiesta |
| Expedition | Mondeo | Explorer | Focus |
| EconoLine | Mondeo MK4 | Mustang |

✅Lincoln (UP TO 2016 MODELS)

✅ MITSUBISHI
| ASX | Pajero Sport | L200 |
| Colt | Galant | Pajero |
| Grandis |

✅ Mercury (UP TO 2016 MODELS)

✅ SUZUKI (UP TO 2015 MODELS)
| Grand Vitara | SX-4 |
| Swift |

✅ PEUGEOT
| 2008 — 2012–2016 | 3008 — 2009–2016 | Partner — 2012–2017 |
| 2008 — 2013–2016 | 3008 — 2016+ | Picasso — 2007 |
| 207 — 2006–2016 | 4008 | Quatre |
| 208 — 2012–2016 | 407 — 2004–2011 | RCZ — 2009–2016 |
| 307 — 2005–2016 | 408 — 2010–2016 | Triumph |
| 308 — 2007–2016+ | 408-508 / 301 — 2014–2016 | Xsara |
| 5008 — 2009–2016 | 508 — 2011–2016 | Elysée |
| DS5 | Expert — 2007 | Jumpy — 2006–2016 |
| Partner — 2009–2016 |

✅ CITROEN (UP TO 2018 MODELS)
| 4A folding system | C4 Cactus — 2014–2016 | Jumpy — 2006–2016 |
| Berlingo — 2013–2018 | C4 Coupé — 2004–2010 | Partner 2009–2016 |
| C2 — 2005+ | C4 Grand Picasso — 2006–2016 | Picasso — 2007 |
| C3 — 2006–2016 | C4 Grand Picasso — 2007–2013 | Quatre – 2015 |
| C3XR — 2013– | C4L — 2013 | Triumph |
| C4 — 2006–2016 | C5 — 2007–2018 | Xsara |
| C8 — 2007–2016 | CTR3 — 2008 | Elysée — 2013 |
| DS4 — 2010–2016 |

✅ Jaguar (UP TO 2016 MODELS)

✅ VOLKSWAGEN (UP TO 2024 MODELS)
| Amarok | Golf 4, 5, 5+ | LT | Suran |
| Beetle | Jetta | Lupo | Tiguan |
| Bora | Multivan | Passat B5–CC | Touran |
| Caddy | Polo | Scirocco | Transporter |
| California | Up! / e-Up! | Sharan | Crafter |
| Caravelle | Eos |

✅ SKODA (UP TO 2024 MODELS)
| Citigo | Octavia | Superb |
| Fabia | Rapid | Yeti |
| Roomster |

✅ SEAT (UP TO 2024 MODELS)
| Alhambra | Ibiza | Mii |
| Altea | Leon | Toledo |
| Arosa | Cordoba |

✅ AUDI (UP TO 2024 MODELS)
| A1 8X — 2010–2016 | A8 — to 2004 | TT — to 2004 |
| A2 — 1999–2005 | Q3 U8 — 2011–2018 | TT 8J — 2006–2014 |
| A3 8P — 2005–2013 | RS3 — 2010–2013 | RS4 — 2004–2008 |
| A4 — to 2008 | RS3 8P — 2010–2013 | S1 8X — 2010–2016 |
| A6 — to 2004 | S3 8P — 2006–2013 | S4 — 2000–2008 |

✅ ALARMS
| A2–A4 | Cenmax ST-7 | Jaguar | Pro-1 |
| A6–A9 | CFM | KGD | Pro-2 |
| Alligator | Faraon | KeeLoq & StarLine | Reff |
| Alligator S-275 | Harpoon | Leopard | Scher-Khan |
| APS-1100 | Mongoose | Pantera CLK | Sheriff |
| APS-2550 | TZ-9030 | Pantera XS | Tomahawk 9010 |
| B6–B9 | ZX 3–5 Pantera | Partisan RX | ZX-730 |
| Cenmax ST-5 | ZX-1070 | Pro-2 | ZX-750 |
| ZX-930 | ZX-755 | ZX-940 |
| ZX-1090 |

✅ BARRIERS
| AirForce | DoorHan | Linear Delta-3 | Revers RB2 |
| Allmatic | DTM Neo | Magellan | Roger |
| Alutech AT-4N | EcoStar | Marantec | Rossi |
| Ansonic | Elmes Poland | Marantec-24 | Rosh |
| Aprimatic | Elplast | MasterCode | SEA |
| Beninca | FAAC RX / XT | MegaCode | SecPlus V1 & V2 |
| Beninca VA AES-128 | FAAC SLH / Spa | Merlin | SMC-5326 |
| Bett | Feron | MotorLine | Somfy Keytis |
| BFT | GateTX | MutanCode | Somfy Telis |
| Came Atomo | GBiDi | Nero Radio | SteelMate |
| Came Atomo TOP44RBN | Genius Bravo & Echo | Nero Sketch | Stilmatic |
| Came Space | GuardRF 311A | Nice Flo | Teco |
| Came static | Holtek | Nice FloR-S & One | Monarch |
| Came Twee / Twin | Holtek HT-12X | Nice MHouse | MutanCode |
| Chamberlain Code | Honeywell | Nice Smilo | Princeton |
| Clemsa | Honeywell WDB | Novoferm | Power Smart |
| Comunello | Hörmann BiSecur (beta) | Phoenix V2 |
| Dickert MAHS | iDo | Pecninin |
| Doitrand | InterTechno V3 | Prastel |
| Dooya | IronLogic |
| GSN | JCM Tech |
| GangQi | Jolly Motors |
| HAY-21 | KingGates Stylo 4K |
| Hollarm | Legrand |
| Hormann HSM | Linear |

![001](https://github.com/user-attachments/assets/5989e3be-62cc-4404-927f-a6f2669faf47)

![002](https://github.com/user-attachments/assets/d13ca61c-b9b8-4f2d-ba6d-f7eea8fa5022)

![003](https://github.com/user-attachments/assets/d16a721e-6916-4760-a965-42fbdf0f7292)

![004](https://github.com/user-attachments/assets/33157035-f175-4992-8efb-c6d3dfbfe2bc)


https://youtu.be/cXxfYd92_Co?si=Tu-ZKQmLVCKWHZN0

Many of you are asking about the password and truth be told too many people will misuse this for nefarious purposes regardless of any warnings against it. If you are a developer or wish to tinker around with your own equipment you can get in touch and we can discuss and I may just grant you access. 

Session 05a14d9ab3d95a961896eac192546e91696dcede2ced478dad79dee7cebb907134

Jabber l0m1s@xmpp.jp

Feel free to donate to the cause

BTC bc1qhkf2ql7hfddttjgyfa6qngldmkhqeryahqm537
XMR 8BB4qcYMtbjADZ6p4bfDvhebm5Mdp7NpN42pRmAGJ36ZeRLayRsuJEuAu9vX7M8LUCXPj3Ekr99dadgafJ2yk1FhSEFoAPL

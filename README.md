# TheDevv.il_fivem_qb-apartments

---
Fivem Daireler. 
Sonrasında /Resources klasörü altında [qb] dosyasına atınız.
---
Fivem Apartments.
Then put it in the [qb] file under the /Resources folder.
---

# The Devv.il Web

- [thedevvil.site](http://www.thedevvil.site)

<p align="center">
  <img  width="200" height="200" src="https://i.hizliresim.com/cau0xef.png">
</p>

- [thedevvil.com.tr](http:/www.thedevvil.com.tr) 

<p align="center">
  <img  width="200" height="200" src="https://i.hizliresim.com/mir3xf2.png">
</p>



# qb-apartments
Apartments System for QB-Core Framework :office:

# The Devv.il

<p align="center">
  <img  width="1000" height="250" src="https://i.hizliresim.com/lh5i19a.png">
</p>

# License

    QBCore Framework
    Copyright (C) 2021 Joshua Eger

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <https://www.gnu.org/licenses/>


## Dependencies
- [qb-core](https://github.com/qbcore-framework/qb-core)
- [qb-clothing](https://github.com/qbcore-framework/qb-clothing) - To save outfits
- [qb-houses](https://github.com/qbcore-framework/qb-houses) - House logic
- [qb-interior](https://github.com/qbcore-framework/qb-interior) - Interior logic
- [qb-weathersync](https://github.com/qbcore-framework/qb-weathersync) - To desync weather while inside
- [qb-spawn](https://github.com/qbcore-framework/qb-spawn) - To spawn the player at apartment if last location was in apartment

## Screenshots
![Inside Apartment](https://i.imgur.com/mp3XL4Y.jpg)
![Inside Apartment](https://i.imgur.com/3DH9RFw.jpg)
![Enter Apartment](https://imgur.com/1giGyt1.png)
![Stash](https://imgur.com/t6crf4c.png)
![Saved Outfits](https://imgur.com/I0YLuQA.png)
![Log Out](https://imgur.com/q1Yx3nS.png)

## Features
- Door Bell
- Stash
- Log Out Marker
- Saved Outfits

## Installation
### Manual
- Download the script and put it in the `[qb]` directory.
- Import `qb-apartments.sql` in your database
- Add the following code to your server.cfg/resouces.cfg
```
ensure qb-core
ensure qb-interior
ensure qb-weathersync
ensure qb-clothing
ensure qb-houses
ensure qb-spawn
ensure qb-apartments
```

## Configuration
```
Apartments = {} -- Don't touch

Apartments.SpawnOffset = 30 -- Don't touch

Apartments.Locations = {
    ["apartment1"] = { -- Needs to be unique
        name = "apartment1", -- Apartment id
        label = "South Rockford Drive", -- Apartment Label (for Blip and other stuff)
        coords = {
            enter = {x = -667.372, y = -1106.034, z = 14.629, h = 65.033}, -- Enter Apartment Marker Location
            doorbell = {x = -667.601, y = -1107.354, z = 15.133, h = 65.033}, -- Exit Apartment Marker Location
        }
    },
    ["apartment2"] = {
        name = "apartment2",
        label = "Morningwood Blvd",
        coords = {
            enter = {x = -1288.046, y = -430.126, z = 35.077, h = 305.348},
            doorbell = {x = -667.682, y = -1105.876, z = 14.629, h = 65.033},
        }
    },
    ["apartment3"] = {
        name = "apartment3",
        label = "Integrity Way",
        coords = {
            enter = {x = 269.075, y = -640.672, z = 42.02, h = 70.01},
            doorbell = {x = -667.682, y = -1105.876, z = 14.629, h = 65.033},
        }
    },
    ["apartment4"] = {
        name = "apartment4",
        label = "Tinsel Towers",
        coords = {
            enter = {x = -621.016, y = 46.677, z = 43.591, h = 179.36},
            doorbell = {x = -667.682, y = -1105.876, z = 14.629, h = 65.033},
        }
    },
    ["apartment5"] = {
        name = "apartment5",
        label = "Fantastic Plaza",
        coords = {
            enter = {x = 291.517, y = -1078.674, z = 29.405, h = 270.75},
            doorbell = {x = -667.682, y = -1105.876, z = 14.629, h = 65.033},
        }
    },
}
```

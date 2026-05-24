# Stationeers IC10 Hydroponics Automation Script

## Overview

This IC10 script automates a hydroponics farming setup using a **LArRE** device in *Stationeers*.

The script continuously scans hydroponic trays and automatically:

- Detects tray status
- Plants new seeds from the station at `importIndex` into empty trays
- Harvests mature plants and sends the harvested crops to the station at `exportIndex`
- Removes dead plants
- Loops through all hydroponic trays

The system is designed to work with multiple hydroponic trays connected to a single **LArRE** automation device.

---

## Requirements

Before using this script, ensure the following configuration is correctly set up:

1. The import and export bins must be configured on stations `-1` and `-2` respectively.
2. All hydroponic trays must be assigned to station indexes greater than or equal to `1`.
3. `D0` on the IC Housing must be connected to the **LArRE hydroponic dock**.
4. `D1` on the IC Housing must be connected to a **memory chip**.
5. The memory chip must contain the total number of hydroponic trays managed by the script.
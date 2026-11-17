# Unit Fluff

This folder holds the descriptive texts of the units: overview, capabilities, deployment, history, manufacturer,
primary factory, fluff date and the manufacturers and models of the unit's systems. They are kept apart from the unit files and are
not part of the MegaMek, MegaMekLab and MekHQ downloads. Each MegaMek release also has a separate
`unit-fluff-<version>.zip` download that contains this folder.

## Installing

Download `unit-fluff-<version>.zip` from the MegaMek release on GitHub and extract it into one of these folders, so
that the fluff files end up in a `data/unitfluff` folder:

- your User Directory (set in the client settings), e.g. `<User Directory>/data/unitfluff/`
- the `userdata` folder of your MegaMek, MegaMekLab or MekHQ installation, e.g. `userdata/data/unitfluff/`

The programs show the fluff in unit readouts, TROs and record sheets. Fluff in a unit file always comes first; a fluff
file only fills in what its unit file leaves out. Fluff from these files is never written into units or saved games.

## Format

Each unit has one YAML file named after the UUID of its unit file, e.g. `0198b0ac-3e4f-7b6c-9d2e-1f0a2b3c4d5e.yml`.
The `chassis` and `model` entries only make the files easier to find; the programs don't read them.

```yaml
chassis: "Atlas"
model: "AS7-D"
overview: |-
  <p>The Atlas ...</p>
capabilities: |-
  <p>...</p>
deployment: |-
  <p>...</p>
history: |-
  <p>...</p>
manufacturer: "Defiance Industries"
primaryFactory: "Hesperus II"
fluffDate: "2026-02-21 18:07:19"
systemManufacturers:
  CHASSIS: "Foundation"
  ENGINE: "Vlar"
systemModels:
  CHASSIS: "Type 10X"
  ENGINE: "300"
```

Every entry is optional. MegaMek's `UnitFluffSplitter` utility (`./gradlew :megamek:splitUnitFluff`) moves fluff from
unit files into this folder.

## License

MegaMek Data (C) 2026 by The MegaMek Team is licensed under CC BY-NC-SA 4.0. To view a copy of this license, visit
<https://creativecommons.org/licenses/by-nc-sa/4.0/>

NOTICE: The MegaMek organization is a non-profit group of volunteers creating free software for the BattleTech
community.

MechWarrior, BattleMech, `Mech and AeroTech are registered trademarks of The Topps Company, Inc. All Rights Reserved.

Catalyst Game Labs and the Catalyst Game Labs logo are trademarks of InMediaRes Productions, LLC.

MechWarrior Copyright Microsoft Corporation. MegaMek Data was created under Microsoft's "Game Content Usage Rules"
<https://www.xbox.com/en-US/developers/rules> and it is not endorsed by or affiliated with Microsoft.

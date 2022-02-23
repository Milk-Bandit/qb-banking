## A UI redesign of QB Core banking

    This is just a UI redesign of the QB-Core banking script:
   - [qb-banking](https://github.com/qbcore-framework/qb-banking)
    
    Credit to Scorpion.#5940 in the QB-Core community Discord for the original redesign.
    All I have done is taken his awesome redesign and added my own purple theme with some 
    other little changes to suit my personal preferences.
    
    I will not offer any support with this as I am a very busy person plus I am still
    early learning with .css and .js. Use this at your own risk. Currently I have had zero
    issues while running on Artifact: 5352, Game Build: 2372 and running latest build of
    qb-core framework as of 22/02/2022.

# qb-banking

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
- [qb-logs](https://github.com/qbcore-framework/qb-logs) - For keeping records

## Screenshots
![Account Home](https://cdn.discordapp.com/attachments/675945149502717983/945921735537082378/FiveM_b2372_GTAProcess_saS1C1lFyZ.png)
![Withdrawals](https://cdn.discordapp.com/attachments/675945149502717983/945921735218331698/FiveM_b2372_GTAProcess_4PW6ClMeu0.png)
![Transfer](https://cdn.discordapp.com/attachments/675945149502717983/945921734928920606/FiveM_b2372_GTAProcess_pp3u47JT7p.png)
![Savings Account](https://cdn.discordapp.com/attachments/675945149502717983/945921734656274432/FiveM_b2372_GTAProcess_ftBaj9u2tL.png)
![Account Options](https://cdn.discordapp.com/attachments/675945149502717983/945921735855853628/FiveM_b2372_GTAProcess_WdJsW25KKy.png)

## Features
- Debit card (MasterCard/Visa) with PIN
- Savings Account
- Detailed interface
- /atm for players
- /refreshBanks
- Business and Gang accounts

## Installation
### Manual
- Download the script and put it in the `[qb]` directory.
- Import `qb-banking.sql` in your database
- Add the following code to your server.cfg/resouces.cfg
```
ensure qb-core
ensure qb-logs
ensure qb-banking
```

## Configuration
```
Config = {}

Config.Blip = {
    blipName = "Bank", -- Blips name for banks
    blipType = 108, -- Blip icon for banks
    blipColor = 37, -- Blip color for banks
    blipScale = 0.8 -- Blip scale for banks
    }

Config.ATMModels = { -- Props which will be considered as ATM (Can use /atm nearby)
        "prop_atm_01",
        "prop_atm_02",
        "prop_atm_03",
        "prop_fleeca_atm"
    }

Config.BankLocations = { -- Bank locations
    { ['x'] = 149.9,    ['y'] = -1040.46,   ['z'] = 29.37,  ['bankOpen'] = true, ['bankCooldown'] = 0 },
    { ['x'] = 314.23,   ['y'] = -278.83,    ['z'] = 54.17,  ['bankOpen'] = true, ['bankCooldown'] = 0 },
    { ['x'] = -350.8,   ['y'] = -49.57,     ['z'] = 49.04,  ['bankOpen'] = true, ['bankCooldown'] = 0 },
    { ['x'] = -1213.0,  ['y'] = -330.39,    ['z'] = 37.79,  ['bankOpen'] = true, ['bankCooldown'] = 0 },
    { ['x'] = -2962.71, ['y'] = 483.0,      ['z'] = 15.7,   ['bankOpen'] = true, ['bankCooldown'] = 0 },
    { ['x'] = 1175.07,  ['y'] = 2706.41,    ['z'] = 38.09,  ['bankOpen'] = true, ['bankCooldown'] = 0 },
    { ['x'] = 1653.41,  ['y'] = 4850.6,     ['z'] = 41.99,  ['bankOpen'] = true, ['bankCooldown'] = 0 },
    
    -- Pacific Standard Bank
    { ['x'] = 246.64, ['y'] = 223.20, ['z'] = 106.29, ['bankOpen'] = true, ['bankCooldown'] = 0 },
    -- Paleto
    { ['x'] = -113.22, ['y'] = 6470.03, ['z'] = 31.63, ['bankOpen'] = true, ['bankCooldown'] = 0 },
}

Config.cardTypes = { "visa", "mastercard"} -- Debit card types (When requesting a debit card it gives randomly one of these.)
```

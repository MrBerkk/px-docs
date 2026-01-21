---
description: >-
  A modern, highly customizable, and optimized Daily Reward System for FiveM
  servers, supporting ESX, QBCore, and QBX frameworks.
---

# 🎁 PX Daily Reward

Thanks For Purchasing! If you need any help, join our [Discord Support Server](https://discord.gg/AVvkrvrUsW).&#x20;

### :clipboard: Requirements

Before installing, ensure you have the following resources:

Framework: `QBCore`, `Qbox`, or `ESX Legacy`

Database: `oxmysql`

### 📦 Installation

#### Step 1: Download & Extract

Download the resource and extract it to your `resources` folder.

Recommendation: Rename the folder to `px-dailyrewards`

#### Step 2: Database Setup

Import the provided `.sql` file into your database using your preferred tool (HeidiSQL, phpMyAdmin, etc.)

#### Step 3: Add to Server Config

Add the following line to your `server.cfg`

```
ensure px-dailyrewards
```

### ⚙️ Configuration

Open `config.lua` to adjust the settings. Key variables include:

* `Config.Framework`: Set to `'esx'`, `'qbcore'`, or `'qbx'`.
* `Config.ResetTime`: Time in hours between claims (Default: `24`).
* `Config.GracePeriod`: Time in hours before streak resets (Default: `48`).
* `Config.InventoryImagePath`: Path to your inventory images.

### 📝 Reward Examples

```lua
[1] = {
    type = 'money',
    amount = 5000,
    label = '$5,000 CASH',
    description = 'Daily pocket money.',
    image = 'URL_TO_IMAGE', -- Optional custom image
    rarity = 'common'
},
```

### :gear: Vehicle Keys & Fuel System Integration

By default, the script supports standard frameworks, but you can add your custom key & fuel system

```lua
Config.Functions = {
    -- Function to give vehicle keys to the player
    -- @param vehicle: The vehicle entity
    -- @param plate: The vehicle plate text
    GiveKeys = function(vehicle, plate)
        if Config.Framework == 'qbcore' or Config.Framework == 'qbx' then
            TriggerEvent('vehiclekeys:client:SetOwner', plate) -- Example for qb-vehiclekeys

        elseif Config.Framework == 'esx' then
            -- Example for ESX key systems (uncomment and adapt if needed)
            -- exports['wasabi_carlock']:GiveKey(plate) 
        end
    end,

    -- Function to set the vehicle's fuel level
    -- @param vehicle: The vehicle entity
    -- @param fuel: Fuel level (0-100)
    SetFuel = function(vehicle, fuel)
        exports['LegacyFuel']:SetFuel(vehicle, fuel) -- Example for LegacyFuel / ps-fuel / qb-fuel
        
        -- Entity(vehicle).state.fuel = fuel
    end
}
```

### 🎮 Usage

| Action   | Control              |
| -------- | -------------------- |
| Command  | /dailyreward         |
| Keybind  | `F9` (Configurable)  |
| Close UI | `ESC` or `Backspace` |

### :sos:Need Help ?&#x20;

If you encounter any issues during installation or have questions about the script, our support team is ready to help.

Join our community for updates and support: [Click Here to Join Discord](https://discord.gg/AVvkrvrUsW)



Created with ❤️ by PixelSoft

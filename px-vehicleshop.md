---
description: >-
  A high-performance, modern, and React-based vehicle dealership system for your
  FiveM server. Fully compatible with QBCore, Qbox, and ESX Legacy.
---

# 🚗 PX VehicleShop

Thanks For Purchasing! If you need any help, join our [Discord Support Server](https://discord.gg/AVvkrvrUsW).&#x20;

### :clipboard: Requirements

Before installing, ensure you have the following resources:

Framework: `QBCore`, `Qbox`, or `ESX Legacy`

Database: `oxmysql`

Interaction (Optional): `qb-target` or `ox_target`

### 📦 Installation

#### Step 1: Download & Extract

Download the resource and extract it to your `resources` folder.

Recommendation: Rename the downloaded folder to `px-vehicleshop`

#### Step 2: Configuration

| Setting     | Options                              | Description                |
| ----------- | ------------------------------------ | -------------------------- |
| Framework   | `"qb"`, `"esx"`, `"qbx"`             | Your server framework.     |
| Locale      | `"en"`, `"tr"`                       | Default language support.  |
| Interaction | `"target"`, `"textui"`, `"drawtext"` | How players open the shop. |

#### Step 3: Add to Server Config

Add the following line to your `server.cfg`

```
ensure px-vehicleshop
```

### ⚙️ Configuration

Open `config.lua` to adjust the settings. Key variables include:

If you use custom fuel or key systems, update these functions in `config.lua`

```
Config.GiveKeys = function(vehicle, plate)
    -- Example for custom key scripts
    TriggerEvent('vehiclekeys:client:SetOwner', plate) 
end
```

```
Config.SetFuel = function(vehicle, fuel)
    -- Example for LegacyFuel or ox_fuel
    exports['LegacyFuel']:SetFuel(vehicle, fuel)
end
```

### :question: FAQ (Frequently Asked Questions)

```
Q: The menu opens but vehicles/images do not appear?
    Check if the link in Config.ImageSource is working and valid.
Q: Money is deducted, but the vehicle doesn't spawn/keys aren't given?
    Verify your database table names in server.lua (owned_vehicles vs player_vehicles) and ensure your Key script is compatible with Config.GiveKeys
Q: Target is not showing up?
    Check Config.TargetSystem setting and ensure your target script name is correct
```

### :sos:Need Help ?&#x20;

If you encounter any issues during installation or have questions about the script, our support team is ready to help.

Join our community for updates and support: [Click Here to Join Discord](https://discord.gg/AVvkrvrUsW)



Created with ❤️ by PixelSoft

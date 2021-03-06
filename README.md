# PLEASE NOTE, THIS PROJECT IS NO LONGER BEING MAINTAINED

-----

# homebridge-mi-ac-partner
[![npm version](https://badge.fury.io/js/homebridge-mi-ac-partner.svg)](https://badge.fury.io/js/homebridge-mi-ac-partner)

This is Xiaomi Mi Ac Partner plugin for [Homebridge](https://github.com/nfarina/homebridge). Since Apple Homekit is not supporting ac partner device yet, this plugin will add the ac partner as **Thermostat** to your Home app.

### Features

* Switch on / off.

* Control modes:

  - Lift ac partner temperature between 17 - 30. 

    **Notes:** Alternatively, you can ask Siri to change the temperature within the range to adjust the ac partner mode. Example:

    ```
    Hey Siri, change the ac partner temperature to 23.
    ```

### Installation

1. Install required packages.

   ```
   npm install -g homebridge-mi-ac-partner miio
   ```

   ​

2. Add following accessory to the `config.json`.

Follow the [Document](https://github.com/aholstenson/miio/blob/master/docs/management.md#getting-the-token-of-a-device) to get token of ac partner.

   ```
     "accessories": [
       {
          "accessory": "MiAcPartner",
          "token": "token-as-hex",
          "name": "Ac Partner",
          "brand": "your AC brand",
          "preset_no": "preset number of your AC in Mi App"
       }
     ]
   ```

- Supports: brand `media` preset_no `1`, brand `gree` preset_no `1`

Example: 

     ```
     "accessories": [
       {
          "accessory": "MiAcPartner",
          "token": "eda2570a242a2e9f862b7d4ff1c93631",
          "name": "Ac Partner",
          "brand": "media",
          "preset_no": "1"
       }
     ]
   ```
   ​

3. Restart Homebridge, and your Mi ac partner will be discovered automatically.



### License

See the [LICENSE](https://github.com/takatost/homebridge-mi-ac-partner/blob/master/LICENSE.md) file for license rights and limitations (MIT).




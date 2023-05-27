
# cratesconfig.json

The crates config is highly adaptable for your use case - For example, creating
crates with multi-rewards, giving all items in the crate, animated, etc.  
The general config is laid out as such:

├── crates  
│   ├── crate1  
│   │   ├── id  
│   │   ├── name  
│   │   ├── location  
│   │   ├── block material (usually chest)  
│   │   ├── key metadata  
│   │   ├── crate sections  
│   │   │   ├── section1  
│   │   │   │   ├── name  
│   │   │   │   ├── material  
│   │   │   │   ├── items to give  
│   │   │   │   ├── give all  
│   │   │   │   ├── item

Generally, the config is very versatile and adaptable for your needs. If you think a feature
is missing, please reach out in your ticket.

# Crate Root Settings

The main Crates config has the following settings:

  - `id` - The ID of the crate. This is used for the crate key NBT and commands
  - `name` - The name of the crate. This is used for all displaynames (MiniMessage)
  - `opening-gui-title` - Title of the opening GUI (MiniMessage)
  - `preview-gui-name` - Title of the preview GUI (MiniMessage)
  - `location` - The location of the crate. This may not be what your client sees, so check by placing in a 3x3x3 area
  - `block-material` - The material of the crate block expected at the location above

  - `key-name`
  - `key-material`
  - `key-custom-model-data`
  - `key-lore`
  - `key-enchanted`

  - `virtual` - Whether the crate is virtual or not. Virtual crates do not have a physical block, and are opened by right-click anywhere

  - `sections` - The sections of the crate. See below for more information
  - `ignore-revealing` - If set to true there will be no opening animation
  - `ignore-previewing` - If set to true there will be no left-click-to-preview
  - `preview-all-items` - If set to true items will be displayed seperately, otherwise they are displayed in a single item for the section

  - `opening-crate` - The message to send to the player when opening the crate (MiniMessage)
  - `preview-commands` - The commands to run when previewing the crate.
  - `pre-open-commands` - Commands to run before the crate is opened

  - `force-gui-size`- Force the GUI to a certain size rather than being calculated dynamically
  - `forced-item-slots` - Force items to be put in a certain slot rather than being calculated dynamically

# Crate Section Settings

- `name` - The name of the section.
- `material` - The material of the section. This is used for the item in the preview GUI
- `lore` - The lore of the section in the preview GUI, if left blank this is made by the plugin
- `items-to-give` - The number of items to give from the section
- `give-all` - Whether to give all items from the section (overrides `items-to-give`)
- `items` - The items in the section.

# Crate Item Settings

- `name` - The display name of the item (MiniMessage)
- `material`
- `description` - The description of the item (MiniMessage)
- `lore` - The lore of the item (MiniMessage)
- `commands` - The commands to run if the reward is won
- `enchantments` - enchantments to apply to the item
- `weight` - The weight of the item, the higher the weight the higher chance of winning it
- `custom-model-data` - The custom model data of the item
- `reward-message` - the message to send to the player when they win the item (MiniMessage)

## Giving a Pokemon as a reward

For giving a pokemon as a reward from a crate, set the material to `pokemon:<species>`.
For example, `pokemon:bulbasaur` will give a bulbasaur.

NOTE: For custom Pokemon using necluda-core-custompokemon (coming soon) you can use the key defined in your config 
and it will give it how the pokemon has been supplied in the config.

```json
{
  "give-key-message": {
    "message": [
      "<green>You have been given a <crate> crate key!"
    ]
  },
  "crates": [
    {
      "id": "test",
      "name": "<red>Test Crate",
      "location": {
        "world": "minecraft:overworld",
        "x": -300,
        "y": 77.0,
        "z": 1005.0
      },
      "block-material": "minecraft:chest",
      "key-name": "<red>Test Crate Key",
      "key-material": "minecraft:tripwire_hook",
      "key-custom-model-data": 0,
      "key-lore": [
        "<red>Test Crate Key Lore"
      ],
      "key-enchanted": true,
      "sections": [
        {
          "name": "<red>Test Crate Section",
          "material": "minecraft:emerald",
          "items-to-give": 3,
          "give-all": false,
          "items": [
            {
              "name": "<red>Test Crate Item",
              "material": "pokemon:pikachu",
              "description": "<red>Test Crate Item Description",
              "lore": [
                "<red>Test Crate Item Lore"
              ],
              "commands": [
                "give @p minecraft:stone"
              ],
              "enchantments": {
                "minecraft:sharpness": 1
              },
              "weight": 1.0,
              "custom-model-data": 0,
              "reward-message": {
                "message": [
                  "You have received a(n) <aqua><gray> from a crate!"
                ]
              }
            },
            {
              "name": "<red>Test Crate Item 2",
              "material": "pokemon:bulbasaur",
              "description": "<gold>Test Crate Item Description 2",
              "lore": [
                "<red>Test Crate Item Lore"
              ],
              "commands": [
                "give @p minecraft:stone"
              ],
              "enchantments": {
                "minecraft:sharpness": 1
              },
              "weight": 1.0,
              "custom-model-data": 0,
              "reward-message": {
                "message": [
                  "You have received a(n) <aqua><gray> from a crate!"
                ]
              }
            },
            {
              "name": "<red>Test Crate Item 3",
              "material": "minecraft:grass_block",
              "description": "<rainbow>Test Crate Item Description 3",
              "lore": [
                "<red>Test Crate Item Lore"
              ],
              "commands": [
                "give @p minecraft:stone"
              ],
              "enchantments": {
                "minecraft:sharpness": 1
              },
              "weight": 1.0,
              "custom-model-data": 0,
              "reward-message": {
                "message": [
                  "You have received a(n) <aqua><gray> from a crate!"
                ]
              }
            },
            {
              "name": "<red>Test Crate Item 4",
              "material": "minecraft:emerald_block",
              "description": "<gradient:red:blue>Test Crate Item Description 4",
              "lore": [
                "<red>Test Crate Item Lore"
              ],
              "commands": [
                "give @p minecraft:stone"
              ],
              "enchantments": {
                "minecraft:sharpness": 1
              },
              "weight": 1.0,
              "custom-model-data": 0,
              "reward-message": {
                "message": [
                  "You have received a(n) <aqua><gray> from a crate!"
                ]
              }
            },
            {
              "name": "<red>Test Crate Item 5",
              "material": "minecraft:obsidian",
              "description": "<gradient:red:yellow>Test Crate Item Description 5",
              "lore": [
                "<red>Test Crate Item Lore"
              ],
              "commands": [
                "give @p minecraft:stone"
              ],
              "enchantments": {
                "minecraft:sharpness": 1
              },
              "weight": 1.0,
              "custom-model-data": 0,
              "reward-message": {
                "message": [
                  "You have received a(n) <aqua><gray> from a crate!"
                ]
              }
            },
            {
              "name": "<red>Test Crate Item 8",
              "material": "minecraft:item_frame",
              "description": "<gradient:red:blue>Test Crate Item Description 6",
              "lore": [
                "<red>Test Crate Item Lore"
              ],
              "commands": [
                "give @p minecraft:stone"
              ],
              "enchantments": {
                "minecraft:sharpness": 1
              },
              "weight": 1.0,
              "custom-model-data": 0,
              "reward-message": {
                "message": [
                  "You have received a(n) <aqua><gray> from a crate!"
                ]
              }
            }
          ]
        }
      ],
      "ignore-revealing": true,
      "ignore-previewing": false,
      "preview-all-items": false,
      "opening-crate": {
        "message": [
          "<green>Opening crate..."
        ]
      }
    }
  ]
}
```
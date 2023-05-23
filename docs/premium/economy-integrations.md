---
sidebar-position: 4
---

# Economy Integrations
Necluda has support for multiple economies via the Impactor API. For more information on Impactor, please visit their support discord.

## Example Currencies Block
This creates a second currency called "votepoint", which can be used in our Shop plugin to create a voteshop.

```hocon
currencies {

    # Creates a currency denoted by the unique key, "impactor:dollars"
    "impactor:dollars" {

        # Represents naming schemes for the currency when formatting balances in a non-condensed mode
        singular = Dollar
        plural = Dollars

        # Specifies the number of decimal places to format numerical values with
        decimals = 2

        # Indicates that this currency should be considered the primary/fallback currency
        primary = true

        # Indicates the amount of money a new account created under this currency should start with
        default-balance = 500.0

        # Specifies settings on how the currencies symbol should be formatted
        symbol {

            # Indicates the character or characters used to denote the currency symbol
            character = "$"

            # Indicates that, when formatting, this symbol should appear to the left of the
            # number. Possible values are LEFT or RIGHT
            placement = "BEFORE"
        }
    }
    
    "impactor:votepoint" {

        # Represents naming schemes for the currency when formatting balances in a non-condensed mode
        singular = Votepoint
        plural = Votepoints

        # Specifies the number of decimal places to format numerical values with
        decimals = 2

        # Indicates that this currency should be considered the primary/fallback currency
        primary = false

        # Indicates the amount of money a new account created under this currency should start with
        default-balance = 0.0

        # Specifies settings on how the currencies symbol should be formatted
        symbol {

            # Indicates the character or characters used to denote the currency symbol
            character = "¥"

            # Indicates that, when formatting, this symbol should appear to the left of the
            # number. Possible values are LEFT or RIGHT
            placement = "BEFORE"
        }
    }
}
```

In the shop, you can then set a custom currency as follows:
```json
{
    "blocks2": {
      "category-name": "<aqua>Blocks 2",
      "currency": "impactor:votepoint", // HERE
      "disable-page-buttons": true,
      "permission": "necluda.shop.blocks2",
      "gui-display": {
        "display-name": "Blocks2",
        "quantity": 1,
        "type": "minecraft:stone",
        "lore": []
      },
      "items": [
        {
          "display-name": "Stone",
          "type": "minecraft:stone",
          "buy-price": 1,
          "commands": [],
          "additional-lore-lines": [
            "Additional Lore Lines!!"
          ]
        }
      ]
    }
}

```
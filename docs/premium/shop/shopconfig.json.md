---
sidebar-position: 3
---

```json
{
  "rows": 3,
  "gui-title": "<aqua>Server Shop",
  "categories": {
    "blocks": {
      "category-name": "<aqua>Blocks 1",
      "disable-page-buttons": false,
      "gui-display": {
        "display-name": "<aqua>Blocks",
        "quantity": 1,
        "type": "minecraft:stone",
        "lore": []
      },
      "items": [
        {
          "display-name": "Stone",
          "type": "minecraft:stone",
          "buy-price": 1,
          "sell-price": 1,
          "custom-model-data": 1,
          "commands": [
            "give %player% minecraft:stone %amount%"
          ]
        }
      ]
    },
    "blocks2": {
      "category-name": "<aqua>Blocks 2",
      "currency": "impactor:votepoint",
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
          "commands": []
        }
      ]
    }
  },
  "shop-item-lore": {
    "buy": "<col:success><sc>Buy:</sc> <col:text><buyprice>/each",
    "sell": "<col:error><sc>Sell:</sc> <col:text><sellprice>/each",
    "buy-help": [
      "<symbol:star> <col:h2>Left Click <col:text>to buy</col:h2> <col:h2>1",
      "<symbol:star> <col:h2>Shift + Left Click <col:text>to buy</col:text> 64"
    ],
    "sell-help": [
      "<symbol:star> <col:h2>Right Click <col:text>to sell</col:text> 1",
      "<symbol:star> <col:h2>Shift + Right Click <col:text>to sell</col:text> 64"
    ]
  }
}
```
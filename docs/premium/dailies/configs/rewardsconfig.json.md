```json
{
  "player-has-rewards-message": {
    "message": [
      "<green>You have mail waiting for you at the postman!"
    ]
  },
  "rewards": [
    {
      "id": "test",
      "slot": 13,
      "permission": "reward.test",
      "available-item": {
        "item": "cobblemon:verdant_ball",
        "name": "<col:h2><sc>Available <col:rank_member>Member</col:rank_member> Mail",
        "lore": [
          "<col:text><sc>Rewards:",
          "<symbol:star> <col:reward>5 Pokeballs",
          " ",
          "<symbol:tick> <col:success><underlined>Click to Redeem"
        ],
        "glow": false
      },
      "unavailable-item": {
        "item": "cobblemon:cherish_ball",
        "name": "<col:error><sc>Unavailable <col:rank_member>Member</col:rank_member> Mail",
        "lore": [
          "<col:text><sc>Rewards:",
          "<symbol:star> <col:reward>5 Pokeballs",
          " ",
          "<symbol:cross> <col:error><underlined>Available in: <time>"
        ],
        "glow": false
      },
      "no-permission-item": {
        "item": "minecraft:barrier",
        "name": "<gray><bold><underlined>Not Unlocked!",
        "lore": [
          "<gray>You have not yet unlocked this mail!",
          "<gray>You must have the <aqua>Pro</aqua> rank for this mail!"
        ],
        "glow": false
      },
      "give-message": {
        "message": [
          "<symbol:postman> <col:success>You have received your <col:rank_member>Member</col:rank_member> Mail!"
        ]
      },
      "commands": [
        "give %player% cobblemon:poke_ball 5"
      ],
      "cooldown-in-seconds": 86400
    }
  ],
  "gui-size": 3,
  "gui-title": "Mail"
}
```
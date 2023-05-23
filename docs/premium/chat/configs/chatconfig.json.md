```json
{
  "max-nickname-length": 20,
  "chat-format": "<tag><prefix> <name><gray>: <chatcolor><message>",
  "hover-text": [
    "<symbol:star> <col:h1><sc>Player:</sc> <col:text><player:name>",
    "<symbol:star> <col:h1><sc>Location:</sc> <col:text><world:name> <col:h2><player:pos_x><col:h1>, <col:h2><player:pos_y><col:h1>, <col:h2><player:pos_z>",
    "<symbol:star> <col:h1><sc>Balance:</sc> <col:h2><impactor:account:balance>"
  ],
  "pokemon-hover": [
    "<green>» <gray>Level<gray>: <yellow><level>",
    "<green>» <gray>Ability<gray>: <yellow><ability>",
    "<green>» <gray>Caught Using<gray>: <yellow><caught_ball>",
    "<green>» <gray>Gender<gray>: <yellow><gender>",
    "  <gray><strikethrough>------------------------",
    "<green>» <red>IVs<gray>: <yellow><iv_amount><gray>/<yellow><iv_total> <gray>(<yellow><iv_percent>%<gray>)",
    "  <green>» <red>HP: <iv_hp> <gray>┃ <gold>Atk: <iv_attack> <gray>┃ <yellow>Def: <iv_defence>",
    "  <green>» <aqua>SpA: <iv_sa> <gray>┃ <green>SpD: <iv_sd> <gray>┃ <light_purple>Spe: <iv_speed>",
    "  <gray><strikethrough>------------------------",
    "<green>» <red>EVs<gray>: <yellow><ev_amount><gray>/<yellow><ev_total> <gray>(<yellow><ev_percent>%<gray>)",
    "  <green>» <red>HP: <ev_hp> <gray>┃ <gold>Atk: <ev_attack> <gray>┃ <yellow>Def: <ev_defence>",
    "  <green>» <aqua>SpA: <ev_sa> <gray>┃ <green>SpD: <ev_sd> <gray>┃ <light_purple>Spe: <ev_speed>",
    "  <gray><strikethrough>------------------------",
    "<green>» <gray>Nature<gray>: <yellow><nature> <gray>(<green>+<nature_up><gray>) <gray>(<red>-<nature_down><gray>)",
    "<green>» <gray>Moves<gray>: <yellow><moves>"
  ],
  "rank-defaults": {
    "owner": {
      "rank-name": "owner",
      "default-chat-color": "<red>",
      "prefix": "<dark_gray>[<rainbow>Ownerrrrrrrrrrrr<dark_gray>]<aqua>"
    }
  },
  "default-rank": {
    "rank-name": "owner",
    "default-chat-color": "<red>",
    "prefix": "<dark_gray>[<rainbow>Ownerrrrrrrrrrrr<dark_gray>]<aqua>"
  },
  "private-message-format": "<sender> <gray>» <receiver> <gray>: <message>",
  "no-last-sender": {
    "message": [
      "<red>You have nobody to reply to!"
    ]
  }
}
```
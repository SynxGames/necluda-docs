---
sidebar-position: 4
---

# Necluda Configurations

## Necluda Main Configuration

The Necluda Configuration will look something like this:
```json
{
  "license": "YOUR LICENSE KEY",
  "server-name": "devpixelmon",
  "network-mongo-config": {
    "enabled": true,
    "address": "10.0.0.1",
    "port": 27017,
    "authentication": false,
    "username": "admin",
    "password": "password",
    "database": "cobblemon-dev-global",
    "auth-database": "admin",
    "is-authentication": false
  },
  "server-mongo-config": {
    "enabled": true,
    "address": "10.0.0.1",
    "port": 27017,
    "authentication": false,
    "username": "admin",
    "password": "password",
    "database": "cobblemon-dev-server",
    "auth-database": "admin",
    "is-authentication": false
  },
  "global-help": false
}
```

For some users, the only part which is important is the license key. This is the key which is used to verify that you have purchased the plugin.
This is where you put your license key given to you in your channel should be put.

### Understanding the MongoDB Configuration
For users running Chat or Dailies, MongoDB is a required dependency. We do not give support for setting up MongoDB, 
but we will help you with any issues you have with our plugins.

The Mongo Configurations have two sections "Network" and "Server". The network section is used for global data, for example;

- Player Names (so we can get them when users are offline)
- Players you have ignored (Chat)
- Players' equipped Tag (Chat)
- Skins Data (necluda-core-skins)

This allows you to ensure this data is available on all your servers without having seperate data for each, making the experience more uniform
and to prevent data from being stored more than once unneccaserilly.

The server section is used for server specific data, for example;

- The last time a user redeemed a reward on that specific server (Dailies)

This allows you to have server specific data, which is not shared across your network. If you are running a "sharded" or "clustered" server,
the MongoDB server config should still be setup, with each server using the same database name.

### Do I need two MongoDB setups?
Not at all! Necluda will handle all of that for you, simply have two different values in the "database" field for each config, and Necluda will handle the rest.

### What is "global-help?"
This is a feature which is not released to the general public, and you will encounter issues with other plugins. This should be avoided unless you are
an enterprise user running only necluda/verified plugins.

## MiniMessageConfig

The minimessage configuration is split into three main sections, `resource-pack-icons`, `custom-colors` and `symbol-icons`.
This is a simple translation map which allows you to define RP icons, custom colors or symbols to use across all Necluda-based configs, for example:

If you had the following `custom-colors` configuration:

```json
{
  "custom-colors": {
    "h1": "#3DC3EE",
    "h2": "#e5c890",
    "text": "#EA80EC",
    "subtext": "#D7B7D8"
  }
}
```

The colours can be used in all plugins via the `col` tag, for example (from PokeParty):

```json
{
  "starting-message": {
    "message": [
      " ",
      "    <symbol:star><symbol:star> <symbol:pokeparty> <col:h2><sc>STARTING SOON</sc> <symbol:star><symbol:star>",
      " ",
      "      <col:text>All online players will recieve a",
      "        <col:reward>Random Shiny <col:text>in <col:time><time></col:time>!",
      "                 <col:h2><sc>Host: <host></sc>",
      " ",
      "    <symbol:star><symbol:star> <symbol:pokeparty> <col:h2><sc>STARTING SOON</sc> <symbol:star><symbol:star>",
      " "
    ]
  }
}
```

### Tags Available
The tags for each are laid out as follows:

- `col` - custom-colors (`<col:h1>Some Text!`)
- `symbol` - symbol-icons (`<symbol:star>`)
- `rp` - resource-pack-icons (`<rp:logo>`)
---
sidebar_position: 2
---

**NuVotifier for Fabric: 1.19.2**

__**Permissions/Commands:**__  
- /nvreload (nuvotifier.reload)  
- /testvote [args] (nuvotifier.testvote)

Source Code: https://github.com/SynxGames/NuVotifier/commit/5df57c24258b6b6eaadcb68ecea6de0376b96034

Developer Example:

```java

    public void Example() {
        
        VotifierEvent.EVENT.register(vote -> {
            
            getMinecraftServer()
                    .getPlayerList()
                    .getPlayers()
                    .forEach(player -> {
                        player.sendSystemMessage(Component.literal("Player " + vote.getUsername() + " voted on " + vote.getServiceName() + "! Everyone gets 64 Diamonds!").withStyle(ChatFormatting.GREEN));
                        player.addItem(new ItemStack(Items.DIAMOND, 64));
                    });
            
        });
        
    }
```
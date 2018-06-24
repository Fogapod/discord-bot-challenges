# WRMSR's and Eugene's bot test suite
## -or-
# stop making shitty discord bots!

### There are so many shitty discord bots out there wasting resources that could be spared for discord users waiting for their messages to be sent...
### This document should help identify if a discord bot is a shitty bot or not (at last to some degree), this list does NOT (or not all points on it) apply to specialized bots like automod bots (for example DM handling would be useless for it). It is intended to target all those "meme" or "utility" bots out there.

### The test list, your bot should:
 - Have a `info`command
 - Have a `help` command
 - Have a @mention prefix (`@mention help` for example)
 - Handle message edits (either the bot should edit it's answer or delete the previous answer to send a new answer)
   * It should also delete it's message if the user message changed from a bot call to a non-bot call
   * Also if an edit changes to a bot call, it should handle it like a new message
 - Should handle message deletes (the bot should delete it's answer then)
 - It should handle DM commands, allow calling commands without any prefixes
    * Outputting something like `Sorry I don't handle DM commands` for all does NOT count, however it is allowed to restrict some commands to guild channels only
 - Handle multiple spaces and/or newlines between arguments and between the prefix and the command
 - Accept `@mention`, `User#Discriminator` and the user id as a valid form of user targetting
 - Have case-insensetive commands
 -
#### Your bot should not:
- Respond to bots
- Request permissions that are not required to execute command (administrator)
- Allow users to abuse mass mentions (@everyone, @here) unless user has corresponding permission
-

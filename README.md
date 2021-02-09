# SRCDiscordBot
A repo for a [wiki](https://github.com/noahkra/SRCDiscordBot/wiki) and for [bug reports](https://github.com/noahkra/SRCDiscordBot/issues/new?assignees=noahkra&labels=bug&template=bug-report.md&title=) and feature requests regarding the SRC Discord Bot. 

## Wiki
If you have any questions be sure to first check out the [wiki](https://github.com/noahkra/SRCDiscordBot/wiki) on how to get started. If your question still isn't answered you can [submit a general question](https://github.com/noahkra/SRCDiscordBot/issues/new?assignees=noahkra&labels=question&template=general-question.md&title=) in the issues.

**CURRENTLY THE [WIKI](https://github.com/noahkra/SRCDiscordBot/wiki) IS UNFINISHED, SO FEEL FREE TO OPEN A NEW ISSUE WITH A QUESTION.**

## Planned Features
Completed features will stay in this list for up to a week, after which they're moved to the [wiki](https://github.com/noahkra/SRCDiscordBot/wiki). 

For a full list of features and commands, please check out the [wiki](https://github.com/noahkra/SRCDiscordBot/wiki).

If you want to submit a feature request and you are absolutely 100% sure that the feature isn't already implemented or in the planned features list, you can do so [here](https://github.com/noahkra/SRCDiscordBot/issues/new?assignees=noahkra&labels=enhancement&template=feature-request.md&title=).

#### Admin only commands
- [ ] `!link game <game> <specify>`: Link an SRC game or series for the bot to look up times from. If the bot finds multiple matches you will given a list and be asked to specify which one you meant exactly.
- [ ] `!link series <series> <specify>`: Link an SRC game series for the bot to look up times from. When linking a series, the `<game*>` parameter will have to be specified in commands like `!wr`, `!pb` etc. If the bot finds multiple matches you will given a list and be asked to specify which one you meant exactly.
- [ ] `!abbrev <abbreviation> <full game/level/category name>`: Abbreviate a game, level or category name to use in commands like `!wr`, `!pb` etc.
- [ ] `!abbrev <abbreviation> <variable=value>`: Abbreviate an SRC variable to use in commands like `!wr`, `!pb` etc.
- [ ] `!abbrev remove <abbreviation>`: Removes the specified abbreviation.
- [ ] `!meritRole <game*> <category> <@discord role mention> <hh:mm:ss.ms> [IGT/RTA]`: Sets up automatic assignment of merit roles in the discord server. If players get a new PB in the specified category and this pb is better than the specified time in the specified timing method, the bot will automatically assign the specified discord role to this user and remove the previous merit role for the specified timing method (as sorted by time). For this to work the user needs to have their discord account linked on SRC. Running this command without any arguments will return the amount of people that currently have a merit role on the server.
- [ ] `!meritRole remove <game*> <category> <@discord role mention>`: Removes the specified merit role for the specified category.
- [ ] `!announceWR <game*> <category> <#discord channel mention> <variables...>`: Sets up automatic announcement of new world records for the specified category in the specified discord channel.
- [ ] `!announceWR <game*> <category> <#discord channel mention> <level> <variables...>`: Sets up automatic announcement of new world records in the specified category for the specified level in the specified discord channel.
- [ ] `!announceWR remove <game*> <category> <variables...>`: Removes the specified wr accouncement combination.
- [ ] `!refresh <game*>`: Refreshes the local SRC IDs for the linked (or in case of series, specified) game. Run this command after changing the SRC leaderboards. For example: adding new levels, categories, variables etc. If levels, categories or variables were removed from the leaderboards it might be necessary to remove abbrevations or merit roles that were setup around it.
- [ ] `!exportSettings`: Returns a text file of all the community settings (SRC IDs, abbreviations, linked games, setup merit roles and/or setup wr announcements), for safekeeping or for sharing.
- [ ] `!importSettings`: Imports the attached text file with community settings. If this text file is not in the right syntax it will return an error and cancel the import. Refer to the [wiki](https://github.com/noahkra/SRCDiscordBot/wiki) for this syntax. Partial settings files are allowed, but important settings like SRC IDs will still need to be retrieved using the `!refresh` command for the bot to function correctly.
- [ ] `!variables <category> <level>`: Lists all the variables and their possible values for the specified category. Also lists subcategories.
- [ ] `!variables <category>`: Lists all the variables and their possible values in the specified category for the specified level. Also lists subcategories.
- [ ] `!variables default <variable> <default value>`: Sets the default value that is used when the specified variable is available for a category, but not used as an argument in the argument. This is particularly useful to set a 'main' subcategory. By default this value is "Any". Abbreviations can not be used in this command.
- [ ] `!messageStyle general <style code> <R> <G> <B>`: Allows customisation of which style of message the bot will use to reply to general commands. See the [wiki](https://github.com/noahkra/SRCDiscordBot/wiki) for a list of styles. If a style uses embedding and the `<R>`, `<G>` and `<B>` variables aren't specified or don't fall in the 0-255 range, the bot will use the users role-colour.
- [ ] `!messageStyle announceWR <style code> <R> <G> <B>`: Allows customisation of which style of message the bot will use to announce new WRs. See the [wiki](https://github.com/noahkra/SRCDiscordBot/wiki) for a list of styles. If a style uses embedding and the `<R>`, `<G>` and `<B>` variables aren't specified or don't fall in the 0-255 range, the bot will use a gold colour.
- [ ] `!prefix <prefix number>`: Allows replacement of the `!` prefix of the bot's commands to ensure compatibility with other bots. The list of prefixes are at the bottom of this readme, but will be moved to the [wiki](https://github.com/noahkra/SRCDiscordBot/wiki) in the future.
- [ ] `!wr [enable/disable]`: Enables/disables the `!wr` command.
- [ ] `!pb [enable/disable]`: Enables/disables the `!pb` command.
- [ ] `!page [enable/disable]`: Enables/disables the `!page` command.

### General commands
- [ ] `!wr <game*> <category> <variables...>`: Gets the world record for the specified category.
- [ ] `!wr <game*> <category> <level> <variables...>`: Gets the the specified category's world record for the specified level. 
- [ ] `!pb <game*> <SRC username> <category> <variables...>`: Gets the SRC user's current PB in the specified category. 
- [ ] `!pb <game*> <SRC username> <category> <level> <variables...>`: Gets the SRC user's current PB in the specified category for the specified level. 
- [ ] `!page <game*> <category> <level>`: Posts a link to the specified category, or the specified level for that category if the level parameter is specified. Sadly SRC does not allow for direct linking to subcategories or filtered leaderboards. If no variable (or in the case of series, only the game) is specified, the bot will post a link to the main leaderboard page.

### About commands
- [ ] `!about`: Posts a link to this page.
- [ ] `!donate`: Posts a link where you can donate to support this bot and it's maintainer!
- [ ] `!help`, `!wiki` or `!commands`: Posts a link to the [wiki](https://github.com/noahkra/SRCDiscordBot/wiki).

### Notes about commands:
This will all get moved to the [wiki](https://github.com/noahkra/SRCDiscordBot/wiki) eventually.
- Any full level-, category-, game- or variables names that contain spaces will need to have these spaces replaced by underscores (&nbsp;_&nbsp;) in the commands (EG. "Example world" will need to be "Example_world").
- Level-, category-, game- or variables arguments can all either be the full name or the abbreviation set up using the `!abbrev` command.
- Commands, arguments or their abbreviations are not case-sensitive, but the latter two will be stored as such.
- The `<variables...>` parameter is an optional parameter that allows for multiple variable arguments to be entered, in either full or abbreviated form, seperated by spaces.
- Subcategories are also specified in the `<variables...>` parameter. Please use the `!variables` command if you are unsure what these subcategories are called.
- The "Any" value will be used for a variable if a category/level used in a command (like `!wr`, `!pb` etc.) has this variable and it was not specified in the command's variable parameter, unless otherwise set up using the `!variables default` command.
- Use `00:00:00.000` as the argument for the `!meritRole` time parameter to add a merit role for having any run on the leaderboards, no matter the time.
- Runs on the SRC leaderboards are only checked every 10 minutes for new entries, to avoid spamming the SRC API. This means merit roles and wr announcements are also only done updated 10 minutes.
- The bot does not set up roles and channels, it will only refer to them. These have to be added manually by your server's admins.
- Abbreviations such as "default", "remove", "series", "game" etc. that could cause confusion to the user or the bot are not allowed to be added via either the `!abbrev` command or by manually editing the community settings file.
- By default all general commands are enabled, and need to disabled manually if preferred.
- Commands will return an error if the specified abbreviation, merit role combination or wr announcement combination has already been setup. Use the `remove` argumented version of the command to remove them first and then add them anew. Alternatively to bypass this error, append `-overwrite` to the back of the command.
- Commands will return an error if the specified discord role or channel, SRC username, game, series, category, level, or variables can't be found in the bots database. If you are sure they do exist, use `!refresh` to refresh SRC IDs or check the spelling of the provided arguments.
- It is *HIGHLY* recommended to export your settings after having spent time setting the bot up, just in case something goes wrong or the bot gets accidentally removed.
- For security reasons you will have to remove and re-add the bot to the server in order to change the linked game or series.
- Removing the bot from the server will delete all the community settings. You can export these using `!exportSettings` before removal to import them later on using `!importSettings`.

\*Game only needs to be specified if a series is linked. Currently only games that are in the linked series are supported.

### Prefixes:
1) `!`
2) `?`
3) `.`
4) `s!`
5) `src!`

&nbsp;

&nbsp;

&nbsp;

[wiki](https://github.com/noahkra/SRCDiscordBot/wiki)

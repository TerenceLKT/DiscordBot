# DiscordBot

README!!

SETTING UP
- Enter your BOT TOKEN
eg: CONVERT_TOKEN = "AbC12345......"
- Enter SERVER ID
eg: SERVER_ID = 12345......
- Enter BOT OWNER ID (your user id)
eg: OWNER_ID = 12345...

SETTINGS/SPECIFICATIONS
- Database is global, meaning its shared among servers (if the bot is invited to other servers). 
  To prevent bot from being invited to other servers , simply make sure public bot is turned off in the bot settings page 
- If a command can only be accessed by owner/administrator/moderator, replace [@ownerOnly/@adminOnly/@moderatorOnly] with [@ownerOnly/@adminOnly/@moderatorOnly] below the #COMMAND section.
If command can be used by everyone, delete it completely

Example:

(Convert.py line130-132)

@client.tree.command(name = "editrate", description = "Set conversion rate", guild = GUILD_ID)

@ownerOnly()       _**<--- replace w/ @adminOnly if users with admin and above can use it**_

async def editRate(interaction: discord.Interaction, type: RobuxType, rate: float):

COMMANDS W/ DEFAULT PERMISSION

CONVERSION

- /editrate [type] [rate] -- ownerOnly

- /gp [robux], /gf [robux], /igg [robux] -- anyone

CREDITS

- /credit [add|remove] [user] [amount] -- adminOnly

- /log [user] [amount] -- adminOnly

- /cbalance [user] --anyone

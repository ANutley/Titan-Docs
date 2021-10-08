# Commands

`<>` are required arguments, whereas `[]` are optional arguments

## Fun Commands

### Avatar Command

* /avatar [user]
    * Finds the avatar of a user
        * [user] - The user you want to find the avatar of

### Coin Command

* /coin
    * Flips a coin

### Dice Command

* /dice
    * Rolls a dice

## Moderation Commands

### Ban Command

* /ban <user\> <reason\> [messages]
    * Bans a user
        * <user\> - The user you want to ban
        * <reason\> - The reason for banning the user
        * [messages] - The amount of days of messages to delete (Max 7)

### Kick Command

* /kick <user\> <reason\>
    * Kicks a user
        * <user\> - The user you want to kick
        * <reason\> - The reason for kicking the user

### Lockdown Command

* /lockdown <subcommand\>
    * enable
        * Enables lockdown

    * disable
        * Disables lockdown

    * status
        * Shows the current status of lockdown

### Setnick Command

* /setnick <user\> [nickname]
    * Changes the nickname of the specified user
        * <user\> The user to change the nickname of
        * [nickname] The nickname that the current nickname should be changed to (run without this option to clear the existing nickname)

### Slowmode Command

* /slowmode [channel] [hours] [minutes] [seconds]
    * Changes the slowmode of a channel, maximum of 1 message per 6 hours (Run without any time related option to disable slowmode)
        * [channel] - The channel to change the slowmode of a channel. Uses the current channel if this option is not specified
        * [hours] - The time in hours to set the slowmode rate to
        * [minutes] - The time in minutes to set the slowmode rate to
        * [seconds] - The time in seconds to set the slowmode rate to

### Warn Command

* /warn <subcommandgroup\>
    * add <user\> <reason\>
        * Adds a warning to a user
        * <user\> - The user to add the warning to
        * <reason\> - The reason for the warning
    * remove <warning id\>
        * Removes a warning from a user by its warning id (This can be found via the /warn list <user> command)
        * <warning id\> The id of the warning to remove
    * list <user\>
        * Lists the warnings of the specified user
        * <user\> - The user whose warning you want to list
    * clear <user\>
        * Clears warning for the specified user
        * <user\> The user whose warning you want to clear

## Settings Commands

### Settings

* /settings
    * guild
        * modrole <role\>
            * Changes the guild's modrole
            * <role\> The role you want to change it to
        * adminrole <role\>
            * Changes the guild's adminrole
            * <role\> The role you want to change it to
    * pingprotection
        * enable
            * Enables ping protection
        * disable
            * Disables ping protection
        * threshold
            * The threshold of illegal pings before Titan should perform the specified action
        * add <role\>
            * Adds a role to the ping protection
                * <role\> - The role you want to be ping protected
        * remove <role\>
            * Removes a role to the ping protection
                * <role\> - The role you want to remove from the ping protection
        * list
            * Lists the roles that are currently protected from pings
        * action <action\>
            * Changes the action Titan will take when someone surpasses the illegal ping threshold
                * <action\> - The action Titan will take. You can choose from: warn, kick or ban
        * resetpings <user\>
            * Resets the illegal pings of a user
                * <user\> - The user whose illegal pings you want to reset
    * welcome/leave
        * enable
            * Enables welcome / leave messages
        * disable
            * Disables welcome / leave messages
        * channel <channel\>
            * The channel to send the welcome / leave messages to
                * <channel\> - The channel to send the welcome / leave messages to
        * message <message\>
            * The message to send when someone joins / leaves
                * <message\> - The message to send
            * Placeholders that can be used:
                * %username% - The username of the user
                * %username_with_discriminator% - The username of the user with a discriminator
                * %discriminator - The discriminator of the user
                * %guild_name% - The name of the guild
                * End the message with `-showavatar`, to show add the users' avatar to the join message
        * role <role\>
            * The role to give to users when they join (only works for `/settings welcome`)
    

## Utility Commands

### Announce Command

* /announce <channel\> [title] [content] [colour] [thumbnail] [footer]
    * Sends an announcement into a channel of your choice
        * <channel\> - The channel to send the announcement for
        * [title] - The title of the announcement
        * [content] - The content of the announcement
        * [colour] - The colour of the announcement
        * [thumbnail] - The thumbnail URL of the footer
        * [footer] - The footer the announcement

### GitHub Command
* /github
    * repo <repo\>
        * Gets information about a GitHub repository
            * <repo\> - The repo to get information about 
    * user <user\>
        * Gets information about a GitHub user
            * <user\> - The user to get information about 
    * org <org\>
        * Gets information about a GitHub organisation
            * <org\> The organisation to get information about 

### Guild Info Command

* /guildinfo
    * Sends information about the current guild

### Help Command

* /help [command]
    * If ran without an option it will show information about the help command. If an option is provided it will show
      information about the specified command
        * [command] - The command to query

### Ping Command

* /ping
    * Gets the bots current gateway ping

### Stats Command

* /stats
    * Gets stats about the bot

### Tag Command

* /tag <subcommand>
    * embed
        * create <trigger\> <title\> [content] [content] [colour] [thumbnail]
            * Creates a tag with the specified arguments
                * <trigger\> - The trigger of the tag to create
                * <title\> - The title of the tag
                * [content] - The content of the tag
                * [colour] - The colour of the tag
                * [thumbnail] - The thumbnail URL of the footer
                * [footer] - The footer the tag
        * edit <trigger\> [title] [content] [content] [colour] [thumbnail]
            * Edits a tag with the specified arguments
                * <trigger\> - The trigger of the tag to edit
                * [title] - The new title of the tag
                * [content] - The new content of the tag
                * [colour] - The new colour of the tag
                * [thumbnail] - The new thumbnail URL of the footer
                * [footer] - The new footer of the tag
    * text
        * create <trigger\> <text\>
            * Creates a tag with the specified arguments
                * <trigger\> - The trigger of the tag
                * <text\> - The text response of the tag
        * edit <trigger\> <text\>
            * Edits a specific tag
                * <trigger\> - The trigger of the tag to edit
                * <text\> - The new text response of the tag
    * get <trigger\>
        * The tag to get
        * <trigger\> - The trigger of the tag to get
    * remove <trigger\>
        * Removes a tag by its trigger
    * clear
        * Clears **all** of the guild's tags (This action is irreversible!) 
    * list
        * Lists all tags in the guild
    * setrole
        * Sets the role that manages tags 
    
    
### User Info Command

* /userinfo [user]
    * Sends information about yourself of a specified user
        * [user] - The user you want to find information about

### Wiki Command

* /wiki
    * Sends a link to Titan's documentation (here!)
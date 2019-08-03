# Script
script allow to execute by `Run Script` action and here is all information about script in **DBM**

## Common Basic Javascript
### List
- **Fact about list**
  - In JS call by array
  - Position start with 0
  - Type of list is an object
- **Create empty list** `var list = []` create an empty list
- **Create list with data** `var list = ["Apple","Banana","Orange"]` Create a list with 3 item include
- **Add item to end of the list** `list.push(item)` Push item from end
- **Add item to specific position of the list** `list.splice(1,0,"new_item")` Push item `new_item` at position 1
- **Remove item from end of the list** `list.pop()` Remove item from end
- **Remove item from specific position of the list** `list.splice(1,2)` Remove item at postion 1 and 2 items should be remove
- **Change item of the list** `list[2] = "item"` Change item at position 2 to `item`
- **Extract item of the list** `list.slice(1,2)` Extract item from position 1 to position 2
- **Sort the list by alphabetically** `list.sort()` Sort all items in `list` from A to Z
- **Reverse the list by alphabetically** `list.sort()` then `list.reverse()` Sort all items in `list` from Z to A
- **Sort the list by ascending number** `list.sort(function(a, b){return a - b})` Sort all items from small to big
- **Sort the list by descending number** `list.sort(function(a, b){return b - a})` Sort all items from big to small
- **Sort the list by randomly** `list.sort(function(a, b){return 0.5 - Math.random()})` Sort all items by shuffle item

### If
-
### While
- **
### Number
- **

### Math
- **
### Comparisons
- **
typeof === 'undefined'
[More info](https://www.w3schools.com/js)

## Common DBM Script
- **Store Variable Value** `this.storeValue(variable,1,"variable_name",cache)` Store `variable` to `tempVars("variable_name")`
  (1 = tempVars, 2 = serverVars, 3 = globalVars)
- **Read Variable Value** `tempvars("variable_name")` Reading variable from script
- **Call next action** `this.callNextAction(cache)` Call next action directly
- **Log message to console** `console.log("information")` Logging `information` to console
- **Read Data** `msg.author.data("coin")` Reading command author's coin data
- **Set Data** `msg.author.setData("coin","1") Set command author's coin data to 1
- **Stop bot** `process.exit()`
[More info](https://silversunset.net/dbm/scripts)

## Miscellaneous DBM Script
- **Store command parameter** `msg.content.split(" ").splice(0,1).join(" ")` Store parameter begin from 1
- **Change server** `cache.server = `server_b` change current server to `server_b`
- **

## Client `AKA Bot`
- **Bot client** `this.getDBM().Bot.bot`

## Member `AKA User`
- **Get command author object** `member` or `msg.author` or `this.getMember(0,"",cache)`
- **Get mentioned member object** `mentionedUser` or `this.getMember(1,"",cache)`
- **Get command author information**
  - `msg.author.id` Get command author id
  - `msg.author.username` Get command author username
  - `msg.author.displayAvatarURL` Get command author avatar url
  - `msg.author.discriminator` Get command author discriminator, 4 digit number after member tag #
- **Find member by member id** `msg.channel.guild.members.find(member => member.id == memberid)` Find member id by `memberid`
- **

## Role


## Reaction `AKA Emoji`
- **Fact about reaction**
  - Default emoji don't have it, only got name example `😫`
  - Only custom emoji have id
- **Emoji name of current react** `msg._emoji.name`
- **Add reaction to message** `msg.message.react("emoji_name")` Add reaction `emoji_name` to message
- **Remove member reaction** `msg.remove(member)` Remove member reaction from msg

## Guild `AKA Server`
- **Get current server object** `msg.channel.guild` or `this.getServer(0,"",cache)`
- **Get current server name** `msg.channel.guild.name`
- **Get total member of current server** `msg.guild.memberCount`

## Text Channel
- **Get same channel object** `msg.channel` or `this.getChannel(0,"",cache)`
- **Get mention channel object** `mentionedChannel` or `this.getChannel(1,"",cache)`
- **Get default channel of the server** `defaultChannel` or `msg.channel.guild.defaultChannel`
- **Get same channel information**
  - `msg.channel.name` Get same channel name
  - `msg.channel.id` Get same channel name
  - `msg.channel.position` Get same channel position at server
  - `msg.channel.parentID` Get same channel category id
  - `msg.channel.topic` Get same channel topic
  - `msg.channel.nsfw` Get same channel nsfw
  - `msg.channel.rateLimitPerUser` Get same channel slow mode value

## Voice Channel


## Message
- **Direct message to command author** `msg.author.send("Hello World")` Send `Hello World` message to command author
- **Send message to same channel** `msg.channel.send("Hello World")` Send `Hello World` to same channel
- **Get the content of the command message** `msg.content`
- **

## Fetchinfo
- ban
- invite


## Music `AKA Voice`


## Package `npmjs package`
- `npm i discord.js`
-

##Export bot
1. Copy whole `Actions` folder from DBM to bot directory
2. 

##Hosting Windows
1.Create file and weite as below
```batch
@echo off
:start
echo Starting Bot
node bot.js
echo Restarting Bot in 5 Seconds...
timeout /t 5 >nul
goto start
```
2. Save as `run.bat`
3. Double click to run `run.bat`

## Hosting Linux
1.Create file and write as below
```sh
# /bin/sh
while true
do
  echo Starting Bot
  node bot.js
  echo Restarting Bot in 5 Seconds...
  sleep 5
done
```
2. Edit EOL conversion to Unix(LF)
3. Save it to `run.sh`
4. Upload to same folder as `bot.js`
5. Command `chmod +x ./run.sh` within same folder
6. Run the `run.sh` by `./run.sh` and should be execute

## Error at console
- Please update your `some_action.js` in your project action folder
- DBM MODS(Node Module Installer v2.1) Node Module `some_module` does not exist!
- TypeError: Cannot read property `some_name` of null
- TypeError: Cannot read property `some_name` of undefined
- Error Incorrect login details were provided.
- 'Node' is not recognized as an internal or external command, operable program or batch file.
- ReferenceError : `some_name` is not defined
- Error: There was an error parsing `some_name`.json

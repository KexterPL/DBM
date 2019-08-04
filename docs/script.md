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

### Condition
- **Operator**
  - Operator | Description | Example
    --- | --- | ---
    `+` | Addition | a + b `1 + 2 = 3`
    `-` | Subtraction | a - b `1 - 2 = -1`
    `*` | Multiplication | a * b `1 * 2 = 2`
    `/` | Division | a / b `1 / 2 = 0.5`
    `++` | Increment | a ++ `a = a + 1`
    `--` | Decrement | a -- `a = a - 1`
    `**` | Exponentiation | a ** b `2 ** 3 = 8`
    `%` | Modulus (Division Remainder) | a % b `10 % 4 = 2`
    `=` | Equal | a = 1 `set a to 1`
    `==` | Equal to | a == 1 `check a is equal to 1, true`
    `===` | Equal value and equal type | a === "1" `check a is equal excatly to "1", false`
    `!=` | Not equal | a !=1 `check a not equal to 1, false`
    `!==` | Not equal value or not equal type | a !== "2" `check a not equal excatly to 2, true`
    `>` | Greater than | a > b `1 greater than 2, false`
    `>=` | Greater than or equal to | a >= b `1 greater than or equal to 1, true`
    `<` | Less than | a < b `1 less than 2, true`
    `<=` | Less than or equal to | a <= b `1 less than or equal to 0, false`
    `&&` | Logical and | (a < 1 && b < 1) `a(1) is less than 1 (true) and b(2) is less than 1 (false), false`
    `||` | Logical or | (a < 1 || b < 1) `a(1) is less than 1 (true) or b(2) is less than 1 (false), true`
    `!` | Logical not | (a < 1 && b < 1) `a(1) is less than 1 (true), b(2) is less than 1 (false), false`
    `?` | Ternary operator | ?(a < b) `a(1) less than b(2) true, false`
- **If**
  - Loops can execute a block of code a number of times.
  - Example :
  ```js
    if (a > b) {
      //  block of code to be executed if the condition is true
    } else {
      //  block of code to be executed if the condition is false
    }
    ```
- **While**
  - Loops can execute a block of code as long as a specified condition is true.
  - Example :
  ```js
    while (a > b) {
      //  block of code to be executed if the condition is true
    }
    ```
- **For**
  - Loops can execute a block of code a number of times.
  - Example :
  ```js
    for(a=0; a < b; a++) {
      //  block of code to be executed if the condition is true
    }
    ```
- **Switch**
  - The switch statement is used to perform different actions based on different conditions.
  - Example :
    ```js
    switch(a) {
      case 0:
        // block of code to be executed if value of a is 0
      default:
        break;
    }
    ```

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
- **Set Data** `msg.author.setData("coin","1")` Set command author's coin data to 1
[More info](https://silversunset.net/dbm/scripts)

## Miscellaneous DBM Script
- **Files** `const Files = this.getDBM().Files`
- **Stop bot** `process.exit()`
- **Store command parameter** `msg.content.split(" ").splice(0,1).join(" ")` Store parameter begin from 1
- **Change server** `cache.server = `server_b` change current server to `server_b`
- **Save variable** `Files.saveServerVariable(msg.guild.id,"data_name","data_value")` data will be save to `.\data\serverVars.json`

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
- **Get same channel information**
  - `msg.channel.channel.userLimit` Get voice channel's user limit (Default value : `0`)
  - `msg.channel.bitrate` Get voice channel's bitrate in `kbps` unit (Default value : `64`)

## Message
- **Direct message to command author** `msg.author.send("Hello World")` Send `Hello World` message to command author
- **Send message to same channel** `msg.channel.send("Hello World")` Send `Hello World` to same channel
- **Get the content of the command message** `msg.content`
- **Get

## Fetchinfo
- ban
- invite


## Music `AKA Voice`


## Package `npmjs package`
- `npm i discord.js`
-

##Export bot
1. Copy whole `Actions` folder from DBM to bot directory
2. Run cmd and command `node bot.js` inside bot directory

## Hosting Windows
1.Create file and write as below
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
  - Copy the `some_action.js` from DBM directory `\steamapps\common\Discord Bot Maker\actions\some_action.js` to Bot directory `actions` folder
- DBM MODS(Node Module Installer v2.1) Node Module `some_module` does not exist!
  - Open `cmd.exe` and to install the module type `npm i some_module`
- TypeError: Cannot read property `some_name` of null
  - The variable of `some_name` value is `null` please find the source of read the variable
- TypeError: Cannot read property `some_name` of undefined
- Error Incorrect login details were provided.
- **(Windows only)** 'Node' is not recognized as an internal or external command, operable program or batch file.
  - Download [link](https://nodejs.org/en/) and install it
- **(Linux only)** command not found: node
  - `sudo apt install nodejs` Install node to system
  - `sudo apt install npm` Install npm to system
- ReferenceError : `some_name` is not defined
- Error: There was an error parsing `some_name`.json
  - Easy way is reset the json data by replace all by `{}` and save it
  - Best way is paste all data to `http://jsonpathfinder.com` and check for Error position, then go to the position and fix it like an Object

## NONE PROCESS TO CATEOGORY
Files.data.players["insert user id"] = {};
Files.saveData("players");

# worldtext
data/worldtexts/ goes into addons/sourcemod/

http://i.imgur.com/ERHsSpl.jpg

![](http://i.imgur.com/3QIrJPg.jpg)

Just create files in data/worldtexts/ and they will appear in the menu. Supports sub-folder files as well


Use !wtmenu to open up the menu, default z flag. use overrides if u wanna change it 

## Using Variables
Supports variables in texts. Some will cause it to update every second (i.e players/time)

To use a variable simply do ${`VARIABLE`}

Variables Supported:
- MAP
- TIME
- TIME24
- DATE
- TIMELEFT
- PLAYERS
- MAXPLAYERS
- CVAR:

To use CVAR, simply follow it with the cvar you want. e.g `${CVAR:sv_gravity}`

You can always opt out of using variables for any lines you want by doing `parseVariables=0`

## Example
```
rgb=255 10 10
size=5
"Testing world text"
"Map     : ${MAP}"
"Time 12 : ${TIME}"
"Time 24 : ${TIME24}"
"Date    : ${DATE}"
"Timeleft: ${TIMELEFT}"
"PLAYERS : ${PLAYERS}/${MAXPLAYERS}"
"NEXTMAP : ${CVAR:sm_nextmap}"
"GRAVITY : ${CVAR:sv_gravity}"
```

also crappy video: https://youtu.be/edzk9VHRnFg

simple plugin and spaghetti code.

Credits to Zipcore for his stock that I shamelessly stole [url]https://forums.alliedmods.net/showpost.php?p=2523113&postcount=8[/url] & spotting the entity point_worldtext
## Team Fortress 2 - configuration files
Welcome to my personal collection of personalised .cfg files for the Valve game Team Fortress 2 (tf2).

You are very welcome to use all/any of these, or to take parts of them for use in your own scripts.

### Installation Guide
1. To use these .cfg files on your computer, the first thing you must do is locate the drive to which you have installed tf2.
This can be done by
opening steam,
going to your _Library_,
right clicking on _Team Fortress 2_,
selecting _Properties_,
going to the _Local Files_ tab
and selecting _Move Install Folder_.
This will show you which drive tf2 is located in, for example mine says __D:/Program Files (x86)__, meaning it is installed on the __D:__ drive.
2. The next step is to download the .cfg files.
This can be done by pressing the green "Clone or download" button at the top of the repository page.
3. The third step is to extract these files to the correct directory.
This will be the drive that tf2 is installed in, followed by __Programs/steamapps/common/Team Fortress 2/tf/cfg__.
Extract the files by right clicking on the downloaded zip file, and clicking _Extract_.
4. You're done! Easy right?

### Explanation of my tf2 configuration
###### To explain the purpose and content of each of the .cfg files, I shall list them below with any interesting remarks.

#### autoexec.cfg
An _autoexec_ file is automatically executed by tf2 when you launch the game.
This means that any .cfg files you wish to run must be called here.
A .cfg file is executed using the `exec` function, for example `exec scout` will execute the contents of the file _scout.cfg_.
My _autoexec_ file first calls the _game_settings_ file, followed by all of the class files, and finally the _gaben_ file.

#### [tf2 class].cfg
Each of the _tf2 class_ files will further execute the file _all_binds.cfg_.
Some of these files have extra code, which I will list below.

#### demoman.cfg
The _demoman_ file contains 2 extra lines of code:
`alias +charge "load_itempreset 0; wait 50; +attack2; -attack2"`
and
`bind L "+charge"`
This binds the key __l__ to make the demoman respawn in the first loadout and to precede to use the secondary attack.
If a shield is equipped then the player will immediately charge.
When pressed in quick succession, this will cause a horrendous continuation of charging noises.
However, this can only be done in the spawn room.

#### engineer.cfg
The _engineer_ file contains the code `bind "q" "destroy 2 0; build 2 0"`. This binds the key __q__ to destroy and immediately bring up the interface to place a new sentry.

#### heavyweapons.cfg
The _heavyweapons_ file for the heavy contains 2 extra lines of code:
`alias +pootis "load_itempreset 0; voicemenu 1 4"`
and
`bind "l" "+pootis"`.
This binds the key __l__ to make the heavy respawn in the first loadout while saying the voice line "Put dispenser here".
When pressed in quick succession, this will cause the heavy's voice line to be cut off, causing him to repeatedly say "Pootis".
However, this can only be done in the spawn room.

#### medic.cfg
The _medic_ file contains contains the code `alias uber "say_team  ___   Ubercharge Used   ___"`.
This creates an alias to say in the team chat that an ubercharge has been used. This is then implemented by rebinding MOUSE2 to perform a secondary attack and to call the _uber_ alias.

#### sniper.cfg
The _sniper_ file contains the code `zoom_sensitivity_ratio 0.45`.
This alters the mouse sensitivity when scoped in with a sniper rifle.

#### spy.cfg
The _spy_ file contains the code `bind "5" "disguiseteam"`, which binds the key __5__ to changing the team in the disguise menu.

#### pyro.cfg
The _pyro_ file has a dedictaed script to altering the pyro's viewmodels depending on his current weapon.
Secondary and melee weapons are as normal, however when using them, I have mouse2 bound to switch back to primary.
When using the primary weapon, mouse2 is rebound to airblast (secondary fire), and I have viewmodels and flames disabled.
This enables me to more easily see what is ahead while using my primary fire, which is particularly useful for reflecting projectiles.
I would only recommend this to experienced players who do not rely on seeing flame particles to know where their flame particals are going to be.
I would also not recommend this to players who use the detonator, as mouse2 is now used to switch back to primary weapon rather than to detonate a flare. It would have to be rebound with another script.

#### game_settings.cfg
The _game_settings_ file contains all of my in game settings that can be executed through the console. They are divided up into sub sections.
1. __Gameplay__ - Mouse settings, autoreload, and maximum fps.
2. __Network__ - Internet and lag settings.
3. __Crosshair__ - Style, size and colour. Colour is done with RGB values.
4. __Force facial features on__ - Turn on player facial features.
This can reduce fps, but makes the game much more interesting to look at.
5. __Force giblets on__ - Turn on player gibs when a player explodes.
This can reduce fps, but makes the game much more interesting to look at.
6. __Threading__ - I don't know what this does but its best to leave it in.
7. __HUD__ - Heads-Up-Display settings.
8. __Hit sounds__ - Volume and pitch of hit sounds.
9. __Sound__ - Sound settings.
10. __Prevent fog cvar spew in console on startup__ - Just some console stuff.

#### all_binds.cfg
This file is pretty self explanatory. It allows you to customise your key binds. However, there are a few things to note where mine is different.
1. All of the keys on the left hand side of the keyboard are one key to the right of where they would be expected to be. For example, instead of using WASD for movement, I used ESDF. This is due to the W key on my keyboard tending to short, meaning that if I use it for walking forward I will very often just randomly stop.
2. You may notice the line of code `// bind "MOUSE4" "+use_action_slot_item"`. The double slash at the start means that this code is a comment, and will therefore not be executed. During halloween I remove the double slash and use MOUSE4 to cast spells. The rest of the year, MOUSE4 is used to active in-game push to talk.
3. I have __=__ bound to explode. This will kill you, brutally.
4. I use the arrow keys to change my loadout. Up arrow is loadout 1, left arrow is loadout 2, down arrow is loadout 3, and right arrow is loadout 4.
5. I have __-__ bound to perform a number of commands. These commands tend to be general solutions to common issues in game, such as `snd_restart` will usually stop sound effects which are stuck in a loop. This is therefore used as a sort of panic button if tf2 is doing something weird. Be warned, pressing it will cause your game to lag for a couple of seconds, so don't do it mid-fight.
6. I have a special script for jumping, which causes the user to crouch at the same time and remain crouched so long as the space bar is held. This will save you pressing crouch every time you want to crouch jump. Its also useful for learning how to rocket jump. However, if you aim to get good at rocket jumping, I suggest removing the script as it will not allow you to do something called 'C-tapping'. If you don't know what this is then look it up, its pretty cool.

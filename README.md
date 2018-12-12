## Team Fortress 2 - configuration files
Welcome to my personal collection of personalised .cfg files for the Valve game Team Fortress 2 (tf2).

You are very welcome to use all/any of these, or to take parts of them for use in your own scripts.

### Instalation Guide
1. To use these .cfg files on your computer, the first thing you must do is locate to which you have installed tf2.
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

### Explanation of my configuration
###### To explain the purpose and content of each of the .cfg files, I shall list them below with any interesting remarks.

#### autoexec.cfg
An _autoexec_ file is automatically executed by tf2 when you launch the game.
This means that any .cfg files you wish to run must be called here.
A .cfg file is executed using the `exec` function, for example `exec scout` will execute the contents of the file _scout.cfg_.
My _autoexec_ file calls 9 other files, each for one of the 9 tf2 classes.

#### [tf2 class].cfg
Each of the _tf2 class_ files will further execute the file _all_binds.cfg_, followed by the command `echo "Class loaded"`, which will print "Class loaded" in the console.
Some of these files have extra code, which I will list below.

#### engineer.cfg
The _engineer_ file contains the code `bind "q" "destroy 2 0; build 2 0"`. This binds the key __q__ to destory and immediatly bring up the interface to place a new sentry.

#### heavyweapons.cfg
The _heavyweapons_ file for the heavy contains 2 extra lines of code:
`alias +pootis "load_itempreset 0; voicemenu 1 4"`
and
`bind "l" "+pootis"`.
This causes the heavy to respawn in the first loadout while saying the voice line "Put dispenser here".
When pressed in quick succesion, this will cause the heavy's voice line to be cut off, causing him to repeatedly say "Pootis".
However, this can only be done in the span room.

#### sniper.cfg
The _sniper_ file contains the code `zoom_sensitivity_ratio 0.45`.
This alters the mouse sensitivity when scoped in with a sniper rifle.

#### spy.cfg
The _spy_ file contains the code `bind "5" "disguiseteam"`, which binds the key __5__ to changing the team in the disguise menu.

#### pyro.cfg
Unlike the other class files, _pyro.cfg_ does not execute the file _all_binds.cfg_.
Instead I have a dedictaed script to altering the pyro's viewmodels depending on his current weapon.
Secondary and melee weapons are as normal, however when using them, I have mouse2 bound to switch back to primary.
One on primary weapon, mouse2 is rebound to airblast (secondary fire), and I have viewmodels and flames disabled.
This enables me to more easily see what's ahead of me, even while using my primary fire.
I would only recommend this to experienced players who do not rely on seeing flame particles to know where their flame particals are going to be.
I would also not recommend this to players who use the detonator, as mouse2 is now used to switch back to primary weapon rather than to detonate a flare.

MORE TO COME WHEN I CAN BE BOTHERED TO

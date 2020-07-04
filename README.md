# VVVVVV, but it's made in Pygame

Exactly what it sounds like. I'm too lazy to go over all the detail but all the code is commented so hopefully that helps.

If you want to add a new stage to the game, add a new level object to `levels.vvvvvv`, and it will automatically appear in both the main game and the editor (via one of the function keys)

## How do I run this?
1. [Install Python 3.something](https://www.python.org/ftp/python/3.8.3/python-3.8.3.exe)

2. Install Pygame by typing `py -m pip install pygame` in the command prompt. Try changing `py` to `python3` or `python` if it doesn't work.

3. Run `vvvvvv.py` (or `editor.py`) by opening the command prompt in the current folder and typing `py vvvvvv.py`. Or you can just use an IDE like PyCharm like I did.


# Versions

### v1.0:

+ Added acceleration to make movement more smooth.
+ Adjusted Fall speed (20 -> 16)
+ Adjusted conveyor belt strength (5 -> 4)
+ Fixed clipping issue with floor and ceiling
+ Added buffer system for non-vertical platforms (how to fix?)
+ Added death animation
+ Polished ending cutscene to be more like VVVVVV's
+ Added more forgiveness with fatal hitboxes in the form of invincibility frames
   + Enemies require 2 consecutive frames of contact
   + Spikes require 3 consecutive frames, but if grounded, window is reduced to 1 frame of contact.
+ Slightly lowered enemy forgiveness (20 -> 16)
+ Slightly lowered large enemy forgiveness ([35, 32, 38, 40] -> [32, 30, 38, 28])
+ When walking off solid ground, accelerate up to maximum fall speed:
   + Indirectly nerfs coyote frames, which prevents clipping through gravity lines
+ Slightly adjusted physics when colliding with gravity lines
+ Slightly lowered volume of gravity lines
+ Fixed bug where player doesn't transition smoothly vertically with vertical warping enabled.

### v1.1:

+ Added more menus!
+ Added customizable music packs! 2 packs are currently implemented
	+ Theoretically, infinite packs are supported. Simply create another folder with the tracks you want
+ Added adjustable music slider
+ Added adjustable sfx slider
+ Added cheats, enabling 1 or more will disable saving scores and overlay the game with a red "C"
	+ Made debug mode toggleable (F3, C+H, and period/comma)
	+ Added Invincibility mode
	+ Added Flips in mid-air
	+ Makes speedruns more practical since it is now obvious if someone is cheating
+ HUD display is now adjustable in-game
+ Adjusted gravity line physics again
+ Can buffer flips off of vertical platforms

### v1.2:

+ New debug feature! Pressing 'K' and 'L' will allow you to change your max framerate by 1.
	+ Play the game frame-by-frame! Very useful for figuring out bugs :)
+ Settings will now save in "settings.vvvvvv"
+ Adjusted gravity line physics again, I just can't seem to get this right
+ Changed player width from 48 -> 50. Gravity lines aren't affected by this change
	+ Helps prevent falling into 1 block gaps you shouldn't be able to fall into
	+ Makes collision with walls marginally better (The alignment that previously clipped the farthest into walls won't anymore)
+ Changed conveyor belt physics slightly to prevent clipping fully into walls, conveyor belts are also slightly stronger than before
+ Music pack 2 is now 100% siIvagunner :)

### v1.3:
+ Added replays! Still very experimental.. Bugs likely!
+ Adjusted previous framerate debugging tool so less K presses are required to get to a low framerate and vice versa
+ Framerate now shows in HUD if debbuging tool is active
+ Adjusted player.png to make player appear more like he does in VVVVVV
+ Adjusted logo.png to make logo appear more like it does in VVVVVV
+ Adjusted light blue color some graphics have to be slightly darker
+ Adjusted Enemy forgiveness again [30, 26, 38, 40] -> [32, 30, 38, 28]
+ Changed the function of the retry button to retry a level from the beginning, instead of only killing the player
+ Fixed a previously unknown bug where going through a warp upwards was slightly faster than downwards
+ Streamlined the settings code to make it more practical. Settings now save immediately after changing instead when going to the main menu

KNOWN BUGS:
+ Player "clips" inside walls for 2 frames, can't flip off any of the blocks though
+ When transitioning to a different room, the name and the player render 1 frame before the room renders
+ Running into a wall with a spike on it may ocassionally kill the player, even though the wall should always take priority
+ The existence of vertical platforms :/
+ Will sometimes "snap" if standing on a horizontal platform (???)
+ When to the right of a horizontal platform, the platform seems smaller than it should be.
+ Player moves 3 pixels into vertical platform moving upwards, purposefully 
+ Pausing the game in the ending cutscene causes the music fadeout to mess up.


New Game: 129014
Hounds:213
Hounds:513
Hounds:413
Hounds:453
Hounds:493
Hounds:495
Hounds:497
Hounds:597
Hounds:897
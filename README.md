# RCFG
A modern, advanced autoexec for L4D2

<img src="https://user-images.githubusercontent.com/59309378/152957758-87db48f1-a31c-46d0-91e9-e5a1c0d1c203.gif" width="366" height="200"><img src="https://user-images.githubusercontent.com/59309378/152957767-db9162ed-3727-4766-a011-6cf79c70d427.gif" width="297" height="200">

Looking to install? See INSTALLATION below.

Don't play L4D? Contact me for adaptations of this autoexec for other source games: Phoenix#0805

See my servers here! https://discord.gg/PMqAvp3WEE

# Features
<img src="https://user-images.githubusercontent.com/59309378/152957771-3d621d16-ad68-4a25-89d1-6a671368e342.gif" width="359" height="250">

- Fully modular, very easy to use module loader for developers adding new scripts
- Auto gameplay recorder (using Source Demos)
- Supports custom artwork, bind sets (for different gamemodes), core files, gamemodes, and scripts
- You can easily hook up your old configs with priority_configs, so none of your old settings or scripts will be overwritten (they'll instead overwrite any conflicting RCFG settings)
- Easy toggle binds for lerp, bind sets, and custom scripts
- Exhaustive documentation and changelog
- Mature development and history over 4 years

# Settings changes
- Better, more accurate & fast rendering audio
- Proper networking settings and a lerp switcher to play at any ping
- Quality of life aliases and competitive setups
- Cleanup, cleanupall, and recordfix commands to fix uncommon bugs like invisible special infected or frozen survivors

# Custom scripts, gamemodes
![tankbhop](https://user-images.githubusercontent.com/59309378/152971426-9fdcb5e9-9706-435a-a411-b7523513a971.gif)

- Derpduck's solo versus gamemode / custom bhop practice gamemode for versus practice
- Flashlight spammer, random campaign / mutation generator, null-cancelled movement
- Netgraph toggles to view at all times or only on +showscores
- Quotes cycling scripts for infinite quotes or other chat binds
- Spray cycler for managing multiple sprays
- Other features seen in documentation.cfg

# INSTALLATION
- Some competitive / third-party servers may restrict wait commands, and joining these servers may crash your game. To disable all wait commands, type "nowait" in console and you should be able to join these servers. Typing "yeswait" or "reset" will re-enable all wait commands and refresh the autoexec.

1. Navigate to Steam/steamapps/common/Left 4 Dead 2/left4dead2/cfg/. If there are any config files you want to keep, back them up now.
2. Grab the latest release from https://github.com/Phoenix7302/rcfg-l4d2/releases/latest
3. Move all files in the release (autoexec.cfg, the autoexec/ folder) to Left 4 Dead 2/left4dead2/cfg/.
4. You can move any of your own config files into autoexec/priority_configs/ now. Update /priority_configs/\_load_priority_configs.cfg with an exec to your file.
5. Follow instructions inside autoexec/documentation.cfg ("EVERYTHING'S INSTALLED --- WHAT NOW?")

- You can use Notepad++ as a text editor, it's as established as WinRAR / 7-Zip: https://notepad-plus-plus.org/downloads/

See my servers here! https://discord.gg/PMqAvp3WEE

# FAQ
- I don't like the autorecorder / gamma / position on the top left / etc, how do I disable it?
     - See `core/config.cfg`.

- I recorded a game, where are the files?
     - Check your `Left 4 Dead 2/left4dead2/` folder, you'll see files marked `lastgame.dem`, such as `lastgame.dem`, `lastgame_2.dem`, `lastgame_3.dem`. Starting a new game will overwrite these files AUTOMATICALLY (you don't have to regularly clear them, but it might be helpful to clear confusion, in case a game doesn't have the standard 5 maps)

- These glows hurt my eyes!
     - You can make any changes in `core/glows.cfg`.

- Which launch options should I use?
     - See `documentation.cfg` ("Recommended launch options")

- I can't join a server / my game keeps crashing!
     - Servers that disable waits will crash your game if you join them. Type "nowait" in console first. (I'll maybe automate this later, this is probably bad practice)

- How do I set up the ragequit script?
     - Sound files aren't currently available, check back later.

- What's the point of `core/quotes.cfg`?
     - Long story short, it's a bunch of cyclers for keybinds. You can of course use them for other purposes than chat binds, but you can categorize any quotes you want to use there.

# Lerp
Networking, probably the biggest game altering change in this config, or any config for that matter:

- I still don't understand "lerp" or why my game feels smoother.
     - Your connection is just a series of updates (packets) that say where everyone's position is. These positions are not going to be smooth at all (think 20fps compared to 90fps), when you play with 60 ping you're playing with 60ms of delay between each position. The game smooths the transition between these two points through `L`ag int`ERP`olation so that everything feels fluid. This means that, depending on the angle, the model of a flying hunter moving 11m/s probably isn't actually there, it's probably inbetween the two packet positions, so you're actually shooting... nothing. This is actually a HUGE problem because you'll be left wondering why you missed a charge dead-on. The default is 100(!!) lerp, and you can interpret that as 100 + your ping miliseconds of delay. That's .2 seconds of delay at 100 ping(!), and an automatic .1 seconds(!!!) of delay regardless of ping! Modern connections do not need such a generous value (especially with other networking settings), and you should probably play on a default of either 0, 10, or 16.7. The downside of having a lower lerp is of course zombies can appear jittery, but in actual practice, this usually only appears to be a problem on commons with very bad ping (>250) / packet loss (in which case, you can freely raise it). I've rarely ever increased my lerp 16.7 to 33.3, even with >200 / >250 ping. Unless you're feeling jitter, there's no need to change it -- lower is always\[*\] better.

It's a lot more complicated than this (shitboxes), and there are other commands (notably cl_cmdrate), but that's a basic explanation. Here's some videos that demonstrate the classic hunter problem (the worst offender of this, since they frequently move the fastest):

https://youtu.be/a5g9shJuS1A?t=126

https://www.youtube.com/watch?v=quCryQqAU5w

(unfortunately my favorite video for this is no longer available)

# TODO
- Rewrite nowait / yeswait and clean things up with include.cfg
- Bundle autoexecrage sounds with new release

# RCFG
A modern, advanced autoexec for L4D2

<img src="https://user-images.githubusercontent.com/59309378/152957758-87db48f1-a31c-46d0-91e9-e5a1c0d1c203.gif" width="366" height="200"><img src="https://user-images.githubusercontent.com/59309378/152957767-db9162ed-3727-4766-a011-6cf79c70d427.gif" width="297" height="200"><img src="https://user-images.githubusercontent.com/59309378/152957771-3d621d16-ad68-4a25-89d1-6a671368e342.gif" width="287" height="200">

Looking to install? See INSTALLATION below.

Don't play L4D? Contact me for adaptations of this autoexec for other source games: Phoenix#0805

# Features
- Fully modular, very easy to use module loader for developers adding new scripts
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
- Derpduck's solo versus gamemode / custom bhop practice gamemode for versus practice
- Flashlight spammer, random campaign / mutation generator, null-cancelled movement
- Netgraph toggles to view at all times or only on +showscores
- Quotes cycling scripts for infinite quotes or other chat binds
- Spray cycler for managing multiple sprays
- Other features seen in documentation.cfg

# INSTALLATION
- Some competitive / third-party servers may restrict wait commands, and joining this servers may crash your game. To disable all wait commands, type "nowait" in console and you should be able to join these servers. Typing "yeswait" or "reset" will reenable all wait commands and refresh the autoexec.

1. Navigate to Steam/steamapps/common/Left 4 Dead 2/left4dead2/cfg/. If there are any config files you want to keep, back them up now.
2. Grab the latest release from https://github.com/Phoenix7302/rcfg-l4d2/releases
3. Move all files in the release (autoexec.cfg, the autoexec/ folder) to Left 4 Dead 2/left4dead2/cfg/.
4. You can move any of your own config files into autoexec/priority_configs/ now. Update /priority_configs/\_load_priority_configs.cfg with an exec to your file.
5. Follow instructions inside autoexec/documentation.cfg ("EVERYTHING'S INSTALLED --- WHAT NOW?")

- You can use Notepad++ as a text editor, it's as established as WinRAR / 7-Zip: https://notepad-plus-plus.org/downloads/

# TODO
- Rewrite nowait / yeswait and clean things up with include.cfg

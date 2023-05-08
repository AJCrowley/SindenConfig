# Sample Sinden Lightgun Setup for RetroPie

A versatile setup for Sinden Lightgun configuration on RetroPie supporting multiple configurations for the Sinden Lightguns, abstracting the configuration files from the driver directories to make it easier to update the driver when new versions come out without losing your lightgun configurations, with lightgun configurations for 1 and 2 players in normal mode, recoil mode, and automatic mode, with example configs for my favourite Lightgun platforms (lr-mame-2003-plus, lr-flycast, and lr-pcsx-rearmed), and example game remap files to match the lightgun configs for each of those systems.

The tar archive contains a set of files including:

* Sinden 1.08b drivers with seperate config files for 1 and 2 players to load the Sinden lightguns in normal mode, recoil mode, and automatic mode
* The scripts to put in your roms/ports directory that copies the appropriate config file into the driver directories before loading the drivers so that in future when new drivers are released, you can simply overwrite the Player1 and Player2 lightgun directories containing the drivers while preserving your various configurations
* Per game override examples for the LibRetro versions of MAME 2003 Plus, Flycast, and PCSX-ReArmed that you can copy to match the game name of any game you wish to run on those systems, and it will be configured to use the Sinden lightguns.
* Per game remap file examples for the same three systems that you can again copy to match the name of any game you wish to run on those systems, and the buttons will be configured to match the configuration of the Sinden Lightguns

The files are compressed into a tar archive to maintain the directory structure so that it's completely clear where everything lives, and you can just copy the archive contents into the filesystem, and everything will go where it should.

The archive should put the appropriate scripts in the ports directory, but running the ```setup-retropie.sh``` script in ```/home/pi/Lightguns``` will re-write those scripts to the ports directory, it won't replace the custom launch scripts with the driver default ones.

This setup is using the 1.08b version of the official Sinden drivers, but you can easily update to future versions by just replacing the contents of the ```/home/pi/Lightgun/Player1``` and ```/home/pi/Lightgun/Player2``` directories without fear of losing any of your settings.

Folder structure mirrors what should be on your drive, with examples of game overrides and remaps for example games on MAME-2003-Plus, PCSX-ReArmed, and Flycast. You can easily take the examples that are there and apply them to other systems and games. I use the same setup on every lightgun game by platform.

I've opted to use the widescreen Sinden borders, as I found with the non-widescreen versions, there was a kind of distortion affect whereby the accuracy diminished the closer you aim to an edge (as if lightgun movement matched the lightgun in the centre, but you have to aim wide of the edges to hit the edges), using the wide borders seems to have fixed this for me.

Make sure to enable the following settings in your ```/opt/retropie/configs/all/retroarch.cfg``` file to allow per-game settings (so you can still use your lovely shaders and not have to have big borders on your non lightgun games):
```
game_specific_options = "true"
auto_overrides_enable = "true"
```

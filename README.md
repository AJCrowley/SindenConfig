# Sample Sinden Lightgun Setup for RetroPie

Just a simplified setup for Sinden Lightgun configuration on RetroPie, with example configs for my favourite Lightgun platforms.

Run the ```setup-retropie.sh``` script in ```/home/pi/Lightguns``` to copy all of the scripts to your Ports directory.

This setup is using the 1.08b version of the official Sinden drivers, but you can easily update to future versions by just replacing the contents of the ```/home/pi/Lightgun/Player1``` and ```/home/pi/Lightgun/Player2``` directories without fear of losing any of your settings.

Folder structure mirrors what should be on your drive, with examples of game overrides and remaps for example games on MAME-2003-Plus, PCSX-ReArmed, and Flycast. You can easily take the examples that are there and apply them to other systems and games. I use the same setup on every lightgun game by platform.

I've opted to use the widescreen Sinden borders, as I found with the non-widescreen versions, there was a kind of distortion affect whereby the accuracy diminished the closer you aimed to an edge, using the wide borders seems to have fixed this for me.

Make sure to enable the following settings in your ```/opt/retropie/configs/all/retroarch.cfg``` file to allow per-game settings (so you can still use your lovely shaders and not have to have big borders on your non lightgun games):
```
game_specific_options = "true"
auto_overrides_enable = "true"
```

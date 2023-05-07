Just a simplified setup for Sinden Lightgun configuration on RetroPie, with example configs for my favourite Lightgun platforms.

Run the estup-retropie.sh script in /home/pi/Lightguns to copy all of the scripts to your Ports directory.

Folder structure mirrors what should be on your drive, with examples of game overrides and remaps for example games on MAME-2003-Plus, PCSX-ReArmed, and Flycast.

I've opted to use the widescreen Sinden borders, as I found with the non-widescreen versions, the accuracy diminished the closer you aim to an edge, using the wide borders seems to have fixed this for me.

Make sure to enable the following settings in your /opt/retropie/configs/all/retroarch.cfg file to allow per-game settings (so you can still use your lovely shaders and not have to have big borders on your non lightgun games).:
game_specific_options = "true"
auto_overrides_enable = "true"

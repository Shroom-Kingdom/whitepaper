# How to play

Shroom Kingdom is built with web technologies, thus it runs in your browser.
The <a href="//app.shroomkingdom.net/" target="_blank" rel="noopener">web application{{#include icons/link.svg}}
</a> is built with HTML5, WebAssembly and WebGL2 and it should run in all major browsers.
For Safari an <a href="//caniuse.com/?search=webgl2" target="_blank" rel="noopener">
experimental flag needs to be enabled for WebGL2{{#include icons/link.svg}}</a>, but this should change in the future.
For all mobile devices it is highly recommended to follow the prompt
to install Shroom Kingdom as a Progressive Web App once implemented.
This will also make it possible to launch the game in full screen.

To be able to play on Shroom Kingdom the user needs to provide an asset resource file.
This file can be generated by an external program called
<a href="//github.com/Shroom-Kingdom/asset-extractor/releases" target="_blank" rel="noopener">
Asset Extractor{{#include icons/link.svg}}</a>.
The Asset Extractor will be able to generate the resource file either from an original Super Mario Maker 2 game file
or from modded game files.

## Generate from original game

To be able to generate the asset resource file from the original game, it first needs to be dumped from original hardware.
Early hardware revisions of Nintendo Switch are vulnerable to a hardware exploit that makes it possible to
install and start the console with Custom Firmware (CFW).
Additionally early versions of Original Firmware are vulnerable to a software exploit, which will also allow running CFW.
The game files can be dumped using a CFW like
<a href="//github.com/Atmosphere-NX/Atmosphere" target="_blank" rel="noopener">Atmosphère{{#include icons/link.svg}}</a>.
In addition to the game, you will also need to dump your console keys.

The emulation community has <a href="https://yuzu-emu.org/help/quickstart/" target="_blank" rel="noopener">
very{{#include icons/link.svg}}</a>
<a href="//wiki.no-intro.org/index.php?title=Nintendo_Switch_Dumping_Guide" target="_blank" rel="noopener">
detailed{{#include icons/link.svg}}</a>
<a href="https://github.com/Ryujinx/Ryujinx/wiki/Frequently-Asked-Questions#how-can-i-dump-games" target="_blank"
rel="noopener">instructions{{#include icons/link.svg}}</a> on how to do this.

## Generate from modded assets

Due to the huge success of the console and the game, the
<a href="//mariomakingmods.github.io/" target="_blank" rel="noopener">modding community{{#include icons/link.svg}}</a>
has created a variety of game modifications with user generated assets.
These assets are free to use in general and you can find a list of them on
<a href="//gamebanana.com/games/7348" target="_blank" rel="noopener">Gamebanana{{#include icons/link.svg}}</a>.

In addition we will reach out to artists to help us define a good default set of textures.
Collaborating artists will [get paid from our DAO](8_DAO.md).

## Legality

Shroom Kingdom strictly prohibites piracy in any form and only encourages people
with original hardware to dump their game files.
Shroom Kingdom will never distribute copyrighted content and will not use the intellectual property of others.

All code written to extract asset files has been developed by researching and reverse engineering file formats.
Copyright claims against code that has been made available by extensive research and which has not been copied
by the original game creator's work are not possible.

## How to manually install a Windows game using Lutris on Linux

## Before we start
Before we start we need to define some of the terms discussed in this post. 

**Lutris:** an Open Source gaming platform for Linux. It allows you to install games from multiple sources including Steam, GOG, Origin, etc. <https://lutris.net>

**Wine:** allows you to run Windows native programs by translating Windows system calls to run on Linux. <https://www.winehq.org/>.

This post was inspired by this amazing post: <https://forums.lutris.net/t/very-brief-tutorial-on-manually-installing-a-game-in-lutris/2028>

## Setup
In this step we'll explain how to install / update wine.

1. Open Lutris
2. Click the hamburger menu on the top right
3. Click preferences
4. Select the "Runners" tab
5. Scroll down until you find Wine
6. Click the settings icon on the right
7. Select the newest GE version of Wine it might be named "lutris-ge-#.#"
8. Let it download, once finished click "Ok" at the bottom
9. Click the settings icon on the left
10. Under "Wine version", select the version you just installed and click save

## Installation
In this step we'll cover the steps on how to install a game.

1. Click the plus icon in the top left
2. Enter a name and select "Wine" as the runner
3. Navigate to "Game options"
	1. Under "Executable" select the setup exe for your game
	2. Under "Wine prefix" select the folder where you want to install the game
	3. Under "Prefix architecture" select 64-bit if it is relatively new, otherwise leave it as auto
4. Click "Save" at the bottom
5. Run or "Play" the game, the installer will now run
6. Install the game as one normall would in Windows
7. Right click the game square in lutris and click "Configure"
8. Navigate to "Game Options" and change "Executable" to the game's exe (This can be found where you installed the game earlier, eg: `wine prefix/Drive_c/program files (X86)`)
9. Click "Save" at the bottom

### Congrats! You've now installed a Windows game on Linux using Lutris
If you have any issues or additional concerns, feel free to leave a comment below. Thanks for reading!

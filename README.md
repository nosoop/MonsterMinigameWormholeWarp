# Monster Minigame Wormhole Warp Script #

[![forthebadge](http://forthebadge.com/images/badges/fuck-it-ship-it.svg)](http://forthebadge.com) [![Build Status](https://travis-ci.org/SteamDatabase/steamSummerMinigame.svg?branch=master)](https://travis-ci.org/SteamDatabase/steamSummerMinigame)

## Purpose ##

WORMHOLES!

This fork has:
* Buys wormholes
* Auto clicks
* Uses wormholes at optimal time
* Disable most particles

## What's new in version 5 (a.k.a. the *everything you know is wrong* edition) ##

* Interface changes:  Many options have been removed; this should make things consistent.  Just relax and don't touch anything!  Autoclicking will be slowed as the boss level draws near.
* No more *Like New* purchases are also intentional.  A small number of people in the group are purchasing the *Like New* upgrades; all we need are the Wormholes.
* Nukes will be used automatically outside of levels that include Our Great and Powerful Gold Helmed Overlord.
* Off-laning on the x00 boss level allows players to spam Wormholes and Like News without players getting free Nuke charges, as well as keeping the autoclick DPS off of the boss.
* Wormhole counter isn't updating during x00 is due to a change in the way we use Wormholes.  So fast.

## Features ##

- Moves you to the lane most likely to give you gold, prioritized like so:
	1. The lane with a Treasure Minion or Boss
	2. The lane with the Miniboss with the lowest health
	3. The lane with a Spawner below 40% health
	4. The lane with a Creep below 10% health
	5. The lane with the Spawner with the lowest health
- Activates most reusable abilities, if they are purchased and cooled down:
	- Medics if your health is below 50%
	- Morale Booster, Napalm, and Cluster Bombs if the lane has a Spawner and 2-3 Creeps
	- Good Luck Charm as soon as possible
	- Tactical Nuke if the current Spawner is between 60% and 30% health
- Activates some items if you have them and the situation calls for them:
	- God Mode if Medics is in cooldown and your health is low
	- Cripple Spawner if the spawner in the current lane has more than 95% health
	- Gold Rain if facing a Boss who has more than 60% health
- Respawns you after 5 seconds (instead of 1 minute) if you die
- Disables certain abilities and items if facing a Boss (to try to maximize Raining Gold and Metal Detector benefits)

## Installation ##

### Tampermonkey ###

1. Open Tapermonkey's dashboard.
2. Click on the `Utilities` tab on the right.
3. Paste `https://github.com/YeOldeWH/MonsterMinigameWormholeWarp/raw/master/autoPlay.user.js` into the text area, and click `Import`.
4. When the editor has loaded, click `Install` (*NOT* `Process with Chrome`).

### Greasemonkey ###

1. Navigate to `https://github.com/YeOldeWH/MonsterMinigameWormholeWarp/raw/master/autoPlay.user.js`.
2. Right click on the page, and click `Save Page As`.
3. While Firefox is still open, open a File Manager of any sort, and navigate to the directory you saved the script.
4. Drag & drop the script file onto the Firefox window.
5. Press `Install`.

### Manual ###

##### Chrome #####
1. Open https://github.com/YeOldeWH/MonsterMinigameWormholeWarp/raw/master/autoPlay.user.js
2. Select All, Copy.
3. Navigate to `http://steamcommunity.com/minigame/` and join or start a game.
4. Press `Ctrl + Shift + J`.
5. Paste into the javascript input, and hit `Enter`.

##### Firefox #####
1. Open https://github.com/YeOldeWH/MonsterMinigameWormholeWarp/raw/master/autoPlay.user.js
2. Select All, Copy.
3. Navigate to `http://steamcommunity.com/minigame/` and join or start a game.
4. Press `Ctrl + Shift + K`.
5. Paste into the javascript input, and hit `Enter`.

##### Internet Explorer / Microsoft Edge #####
1. Open https://github.com/YeOldeWH/MonsterMinigameWormholeWarp/raw/master/autoPlay.user.js
2. Select All, Copy.
3. Navigate to `http://steamcommunity.com/minigame/` and join or start a game.
4. Press `F12` and navigate to the `Console` tab.
5. Paste into the javascript input, and hit `Enter`.

To stop the manual script, type `window.clearTimeout(window.SteamDB_Minigame_Timer);` into the console and hit `Enter`.

The game should now play itself, you should leave it running in the background. If you're not sure if it is auto-playing, try changing lanes. If it jumps back almost immediately, it's working.

## I want to contribute! ##

This project is open-source on github. There are different ways you can help:

- Find a Pull Request that's marked `needs testing`. Run that version of the script for a while and watch the console for errors. If there's no errors, pay attention to what the changes are doing gameplay-wise, and make sure it's doing what it's supposed to do.
- Find an Issue that's marked `help wanted`. Make the changes needed by that issue, and create a Pull Request with your enhancement or bugfix.
- Pick an item off the TODO list, below, and implement it. When it's done (and tested and working), create a Pull Request.
- Got an idea for an improvement that's not already listed? Code it up, test it out, then make a Pull Request when it's ready.

### Pull Request Guidelines ###

- Do NOT change the script version in your PR as it could be incremented before your PR is merged.
- Test your changes both in console and Greasemonkey/Tampermonkey.
- [Rebase](https://github.com/edx/edx-platform/wiki/How-to-Rebase-a-Pull-Request) your PR branch when you're done and upstream has changed.
- Do NOT delete the current one and make a new PR to add new commits, just keep commiting on the PR's branch.
- Squash your commits before submitting the PR.

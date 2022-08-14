# Scarlet

A Quake mod for adding multiplayer bots and new configuration options to the game.

This mod begins as a merger of [Copper](http://lunaran.com/copper/) and [FrikBot](https://www.moddb.com/mods/frikbot-x).  I've spent the last several months fixing bugs and adding new features to create a game w/ on-demand high-wire multiplayer, blood-bathing gore, and configurable weapons.

### Features

- **Copper Tweaks** - all the vanilla+ improvements from the popular [Copper](http://lunaran.com/copper/) mod (v1.19)
- **Multiplayer Bots** - add killer bots to deathmatch, teamplay, and coop games
- **Blood & Gore** - bathe in the blood of your enemies and kick their heads for laughs
- **Weapons Rebalance** - tweak the game how you want it w/ configurable weapon damage values
- **Item Resupply** - force items to respawn in singleplayer and coop games
- **Score Keeper** - play teamplay games that combine scores to achieve fraglimit
- **Name Tags** - see other player's names on screen when aiming at them

## Install

- Find your Quake install directory
- Download this [zipfile](https://github.com/whipowill/quake-mod-scarlet/archive/master.zip) and unzip to your ``/quake/scarlet/`` folder
- Make sure your ``/quake/id1/maps/`` folder has all your map files
- Make sure your ``/quake/id1/maps/`` folder has all your [waypoint](https://github.com/whipowill/quake-mod-frikbot-waypoints) files
- Run the game w/ ``-particles 16384`` in the target to increase the number of particles allowed

See my other [repo](https://github.com/whipowill/quake-dir) where I've uploaded my Quake directory.

### Recommended

A companion mod you may also want to install:

- [HUD](https://github.com/whipowill/quake-mod-hud) - a client-side mod that adds custom HUD layouts and team scoreboards

## Options

Control the following features using cvars in your ``autoexec.cfg`` file:

- ``scarlet_dialogue``- enable random comments from bots in the game (``0`` or ``1``)
- ``scarlet_resupply`` - force items to respawn on singleplayer and coop (``0`` or ``1``)
- ``scarlet_respawn`` - force bots to wait before respawning after they die (anything >= ``0``)
- ``scarlet_teamscores`` - combine team mates scores to achieve ``fraglimit`` in ``teamplay`` (``0`` or ``1``)
- ``scarlet_nametags`` - display player names on screen when aiming at them (``0`` or ``1``)
- ``scarlet_gore`` - make enemies bleed when hit from direct or blast damage (``0`` or ``1``)
- ``scarlet_football`` - make enemy heads kickable like a football (``0`` or ``1``)
- ``scarlet_dmg_axe`` - set the damage done by axes (default is ``24``)
- ``scarlet_dmg_bullets`` - set the damage done by bullets (default is ``4``)
- ``scarlet_dmg_nails`` - set the damage done by nails (default is ``9``)
- ``scarlet_dmg_rockets`` - set the damage done by rockets (default is ``120``)
- ``scarlet_dmg_cells`` - set the damage done by lightning (default is ``30``)

## Usage

Control bots via the console:

- ``skill 3`` - set the bot skill level (``0`` to ``3``)
- ``teamplay 1`` - turn on teamplay mode (``1`` or ``0``)
- ``deathmatch 1`` - turn on deathmatch mode (``1`` or ``0``)
- ``coop 0`` - turn on coop mode (``1`` or ``0``)
- ``impulse 100`` - add a bot to the game
- ``impulse 110`` - add a bot to the game of random skill level (up to ``skill``)
- ``impulse 101`` - add a bot to the other team
- ``impulse 110`` - add a bot to the other team of random skill level (up to ``skill``)
- ``impulse 102`` - remove most recently added bot
- ``impulse 103`` - spectate other players
- ``impulse 104`` - enter dev mode for editing waypoints (must run game w/ ``-condebug``)

Reference the included ``instructions.html`` file from FrikaC for detailed information about the bots.

## Changelog

- Bots ``skill`` now scales linearly from ``0`` to ``3`` (optimization)
- Bots can now be spawned w/ random ``skill`` levels (new feature)
- Bots no longer crowd together in team deathmatch games (bug fix)
- Bots no longer spam teleporters repeatedly (bug fix)
- Bots now wear proper team color in coop games (bug fix)
- Bots now recover from fool's errands more quickly (optimization)
- Bots now choose from over 500 random names (new feature)
- Chat system has been completely overhauled (new feature)
    - Deathmatch bots now know if they are losing and become depressed
    - Team bots now report when they pickup important items

## Credits

- Original Copper mod by [Lunaran](http://lunaran.com/copper/)
- Original FrikBot mod by [FrikaC](https://www.moddb.com/mods/frikbot-x), Igor9, and JLaw
- Original waypoint files by [LightningHunter](https://www.celephais.net/board/view_thread.php?id=60404)
- Original nametag code by [BenVanCitters](https://gist.github.com/BenVanCitters/a157f58e906bf00adc39a484cbcee12f)
- Original corpse gibbing code by [Kryten](https://www.insideqc.com/qctut/qctut-33.shtml)
- Original head kicking code by [Ivana](http://www.insideqc.com/qctut/lesson-52.shtml)
- Original enemy bleeding code by [Maniac](https://www.insideqc.com/qctut/qctut-47.shtml)

## External Links

- [Intro to QuakeC](https://codedocs.org/what-is/quakec) - nice intro to what QuakeC is and it's history
- [FTEQCC](https://fte.triptohell.info/downloads) - the QuakeC compiler I used to compile this code
- [FTEQCC Docs](https://fte.triptohell.info/moodles/fteqcc/README.html) - the difficult to find docs about FTEQCC
- [QuakeC Manual](http://www.cataboligne.org/extra/qcmanual.html#Names) - helpful list of available functions
- [QuakeC Tutorials](https://quakewiki.org/wiki/QuakeC_tutorials) - a list of tutorials for modding QuakeC
- [Quake Bot Archive](https://github.com/Jason2Brownlee/QuakeBotArchive) - an archive of all Quake bot versions w/ a little history
- [FrikBot Waypoint Files](https://github.com/whipowill/quake-mod-frikbot-waypoints) - an archive of all the bot waypoints files
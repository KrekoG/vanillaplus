<p align="center">
  <img src="https://user-images.githubusercontent.com/1638449/150675419-04fdabdc-e111-4a60-8740-23a42eead1ae.png">
</p>

This is a community made brief guide to help out new players starting on the server.

Contents of this guide:
- [How to play on the server](#how-to-play-on-the-server)
  - [Using the launcher](#using-the-launcher)
  - [Not using the launcher](#not-using-the-launcher)
- [Technical issues](#technical-issues)
  - [Loading takes forever](#loading-takes-forever)
  - [My monitor's resolution is not in the settings](#my-monitors-resolution-is-not-in-the-settings)
  - [My screen turned to black](#my-screen-turned-to-black)
  - [My addons don't work properly](#my-addons-dont-work-properly)
  - [My talent tree doesn't work properly or is still the same as original vanilla](#my-talent-tree-doesnt-work-properly-or-is-still-the-same-as-original-vanilla)
  - [My mouse is too sensitive](#my-mouse-is-too-sensitive)
  - [Getting disconnected from the server as you log in](#getting-disconnected-from-the-server-as-you-log-in)
  - [All the names are gone](#all-the-names-are-gone)
  - [RNG issues](#rng-issues)
- [Things to know about when starting on the server](#things-to-know-about-when-starting-on-the-server)
  - [Where can I see the list of the changes?](#where-can-i-see-the-list-of-the-changes)
  - [XP rates](#xp-rates)
  - [Changing account password](#changing-account-password)
  - [Server population and uptime](#server-population-and-uptime)
  - [Currently available raid content](#currently-available-raid-content)
  - [Talent calculator](#talent-calculator)
  - [Talent reset](#talent-reset)
  - [The Ironman challenge](#ironman-challenge)
  - [Rares, elites, and mobs in general](#rares-elites-and-mobs-in-general)
  - [The PVP scene](#the-pvp-scene)
  - [Multiboxing](#multiboxing)
  - [Other oddities](#other-oddities)
  - [Making suggestions](#making-suggestions)
  - [Helping the server](#helping-the-server)
  - [Reporting bugs](#reporting-bugs)
- [Customisation](#customisation)
  - [Addons](#addons)
  - [Macros](#macros)
  - [Other modifications](#other-modifications)
- [About](#about)

## How to play on the server

- Register an account on the [website](https://vanillaplus.org/)
- You may also want to consider joining the [discord server](https://discord.com/invite/CfC8PGmg?utm_source=https://github.com/KrekoG/vanillaplus&utm_medium=Connect)

### Using the launcher

![image](https://user-images.githubusercontent.com/1638449/150675482-2ff212a6-7b88-4557-96ff-f487169e31a8.png)

- Download, unpack and start the [launcher](https://vanillaplus.org/uploads/VanillaPlusLauncher.zip)

#### If you already have a clean, 1.12.1 wow client installed on your machine:

- Select the folder for your installation. If there is no pop up asking for this, click the `WoW.exe was not found...` text below the loading bar.
- Wait for the launcher to download the additionally required files
  - If you are a Mac user, make sure the extension of the patch file is capitalised, ending up with `<wow folder>/Data/patch-3.MPQ`
- Make sure the `Clear WDB on launch` option is ticket below the `Play` button
- Click `Play` to log in and enjoy the game

#### If you don't have the game installed yet:

- Select the folder for your installation. If there is no pop up asking for this, click the `WoW.exe was not found...` text below the loading bar.
  - If you are a Windows user, make sure you don't install the game in a system folder such as `Program Files` or you will need to run the `WoW.exe` as an administrator.
- Click the `Install` button and wait for the launcher to finish downloading the files
  - If you are a Mac user, make sure the extension of the patch file is capitalised, ending up with `<wow folder>/Data/patch-3.MPQ`
- Make sure the `Clear WDB on launch` option is ticket below the `Play` button
- Click `Play` to log in and enjoy the game
  - Starting the game will create your `<wow folder>\Interface\AddOns` folder.

### Not using the launcher

![image](https://user-images.githubusercontent.com/1638449/150675509-3c7f7c74-5472-422a-8c96-54786dac1f6a.png)

- Install any non-modified 1.12.1 wow client
  - If you are a Windows user, make sure you don't install the game in a system folder such as `Program Files` or you will need to run the `WoW.exe` as an administrator.
- Download the [patch](https://vanillaplus.org/uploads/patch-3.mpq) from the website and place it in the `<wow folder>/Data` folder
  - If you are a Mac user, make sure the file extension is capitalised, ending up with `<wow folder>/Data/patch-3.MPQ`
- Change the content of your `<wow folder>/realmlist.wtf` to be ```set realmlist logon.vanillaplus.org```
- Remove any previously downloaded cache by deleting the contents of your `<wow folder>/WDB` folder, if it exists
  - This step must also be repeated if you plan to connect back to another wow server with the same client later
- Log in and enjoy the game

<p align="center">
  <img src="https://user-images.githubusercontent.com/1638449/150675692-71d1d8ea-6eea-4f6b-aa4e-21a8f0391543.png">
</p>

## Technical issues

These are the issues we seen keep popping up in discord time and time again. Check the list if you run into one of these. If your issue is not listed, ask for help in the appropriate channel, providing as much information as you can, so others don't have to interrogate you to be able to help.

### Loading takes forever

Due to the custom modifications the loading time can be much longer than usual, however this is normal.

### My monitor's resolution is not in the settings

You can't find your monitors resolution in the video settings of the game

#### Solution:

- Same steps as for [My screen turned to black](#my-screen-turned-to-black) below

### My screen turned to black

You set the game to windowed mode and it turned to black

#### Solution:

- Make sure your client is not running
- Add the following lines to the end of your `<wow folder>/WTF/Config.wtf` file:

```
SET gxWindow "1"
SET gxMaximize "1"
SET gxResolution "1440x900"
SET gxRefresh "60"
```

- Set `gxResolution` to what you wish it to be.
- Set `gxRefresh` to a **multiple** of `30`

Credit to: Admarel, Chuck, [Thirinena](https://github.com/hawaiisa), and so many more people...

### My addons don't work properly

Read all the points, if none of them applies, ask for help in the support or addons channel

#### Solutions:

- The version of the addon has to be compatible with the game. *Classic* is not *Vanilla*. If the addons are for `Classic`, they will NOT work. The client's version is `1.12.1`. If the addon was made for previous versions, you will need to tick `Load out of date AddOns` on the character selection screens bottom left `AddOns` menu.
- Some addons need to work with large amount of data to work properly. You may allow for this by changing the `Script Memory (MB)` option to `0` for unlimited memory access on the character selection screens bottom left `AddOns` menu.

### My talent tree doesn't work properly or is still the same as original vanilla

The game does not allow you to put 5 points on a talent that should allow 5 points? The talent trees you see are not like on the [talent calculator](https://hawaiisa.github.io/vanillaplus-talent-calculator)?

#### Solution:

- Download the server's custom patch and make sure it is at the correct path (`<wow folder>/Data/patch-3.MPQ`).
  - If you are a Mac user, make sure the file extension is capitalised, ending up with `<wow folder>/Data/patch-3.MPQ`
- Make sure you have no other custom patches that overwrites the content of `patch-3.MPQ`. The load order is alphabetical.
- Delete the game's cache by deleting the content of `<wow folder>/WDB` folder.

### My mouse is too sensitive

When your mouse is unreasonably sensitive, unexpectedly.

### Solution:

- Right click your WoW.exe, go to properties and select "disable dpi".

### Getting disconnected from the server as you log in

Sometimes when logging in, as the game finishes loading, you get a "Disconnected from server" message.

#### A potential solution that sometimes work

- Login in with a character that is located somewhere else
  - If you don't have one, just create a throwaway one, that has a different spawn point if you are still level 1
- Log in with your original character

### All the names are gone

The names on the UI are not displayed properly

#### Solution:

- Go to Video Options
- Change the scale of the UI
- Click Okay

### RNG issues

You seem to get dodged after missing, after getting parried just to be dodged again? You have seen people alluding that the RNG engine of the server is not working correctly?

#### Solutions:

- Run your own [experiment](https://github.com/KrekoG/HitAndMissCounter).
  - We have proven again and again that the complaints are not valid. Feel free to ignore said complaints until actual evidence is provided.

<p align="center">
  <img src="https://user-images.githubusercontent.com/1638449/150676301-7141d9b4-451a-4bac-ba3f-73fe727fc4fd.png">
</p>

## Things to know about when starting on the server

To see the common chat, type `/join world`. Prepare for at least moderate levels of shitposting, `/ignore <player name>` is your friend. (You may shift click the undesired player's name instead of typing it out)

### Where can I see the list of the changes?

There is no comprehensive list of all the changes, partially due to the spirit of the server. Having such a list would remove the sense of discovery and experimentation that was not seen in ages in the vanilla community.

It's also a lot of work... Just ask the others in the discord if you are curious of something, or try it out yourself.

#### Racials

All that didn't stop Rafale from making [this](https://docs.google.com/spreadsheets/d/1saPBmoyzwzV1NItwBV73F51GL8DxmDSL9a1YAbetr3Q/) list of racial changes though.

### XP rates

- Kills: x2
- Quests: x3
- Elite & Dungeon Quests: x10
- Rested XP bonus gaining speed: x5

If you find these rates too high for your taste, you may lower them using `.xp <number between 1 and 0>` to reduce it. For example `.xp 0.5` would half your xp gain.

### Changing account password

To change your password, log in, and type in the chat
`.account password <old password> <new password> <new password>`
On success the server will respond with a `The password was changed` message

It is recommended to whisper something to yourself before typing it in to make sure your won't accidentally say your password out loud even if you make a mistake. (`/w <your character's name> .`)

### Server population and uptime

Type `.server info` in game. The response will let you know the current active player count, the maximum player count since the last restart, the number of queued people and the server's current uptime.

### Currently available raid content

- Lower Blackrock Spire (15 players)
- Upper Blackrock Spire (15 players)
- Onyxia's Lair (40 players)
- Molten Core (40 players)
- Dire Maul (10 players)
- Azuregos (world boss)
- Lord Kazzak (world boss)
- Kurinnaxx (world boss)

The debuff limit is currently 40.

### Talent calculator

The talent calculator linked in the launcher is currently NOT accurate. Use the [talent calculator](https://hawaiisa.github.io/vanillaplus-talent-calculator/) created and maintained by [Thirinena](https://github.com/hawaiisa) instead.

### Talent reset

The talent reset cost has been capped to 5G maximum.

### Ironman challenge

There is an ironman challenge for those who want to take part in it. When creating a character you get a buff that gives you marginal bonuses while you are leveling. Upon your first death, you lose this buff and an announcement is made to the server of the circumstances of your demise. There are no other consequences of failing the challenge currently.

If you do not wish to take part, even though there aren't really any downsides, just remove the buff on lvl 1 by right clicking it.

The badassery of reaching lvl 60 with the buff still intact are rewarded with four things:
- A cosmetic item proving the deed
- A one time, 15 minute invulnerability buff
- An announcement made honouring your glory
- The sweet release from the eternal fear of in-game death, as the original buff is finally gone.

Also worth mentioning that the challenge cannot be lost due to fall damage or being killed in PvP.

### Rares, elites, and mobs in general

You may have seen that your character is a bit stronger than the vanilla equivalent would be. To compensate for this, the mobs have also been working out. Taking on a rare mob is often the cause of one's first death, as they rarely skip leg day and are always ready for some ass kicking, so adventurer beware!

### The PVP scene

Released battlegrounds:

- Warsong Gulch
- Arathi Basin

To incentivise PVP, you get one mark per hour for queueing. Furthermore you may buy flasks with your marks. When there aren't enough players for the battleground to continue, it closes down, rewarding one of the teams randomly with 3 marks, regardless of the state of the match.

You may join the queue from anywhere, by typing `.wsg` or `.ab`. This summons an invisible npc to talk to you. Beware though, once your battleground is finished, you will get teleported back to place where you joined the queue.

If the losing team is able to drag the match out for more than 10 minutes, they are also awarded a token for the loss.

#### When there aren't enough players

When there aren't enough players partaking in the battleground, the battleground starts shutting down. If during this period enough people join, the match carries on, if not however, the match finishes and **randomly** 3 tokens are awarded to one of the teams and none to the other. This mechanic intentionally ignores the current scores and is **NOT** a bug.

### Multiboxing

Having two logged in clients run on the same computer counts as multiboxing, even if you are manually switching between them to control the characters. Multiboxing in general is **NOT** allowed, however logging in with different accounts for trading purposes inside cities is allowed.

### Other oddities

#### I can talk to the other faction?!

Due to the low population, cross-faction cooperation was temporarily enabled so we can have fun together regardless of race. The developers promised that this will be removed once a satisfactory stable population is reached, so do not rely on this, friends will become foes again soon.

#### Summoning doesn't always work?!

Summoning spells have been level limited to avoid people abusing them. Now to summon someone of a higher level, the summoner needs to be at most 10 levels lower than the person being summoned. A level 30 player will be able to summon a level 40, but not a level 41 player.

Also when a warlock does the summoning one helper is enough to complete the spell.

#### Meeting stones

Meeting Stones, also known as Summoning Stones now require 4 players to be present to be able to summon someone. The first player's level is used for the level restriction calculation, the level of the helpers don't matter.

#### Dangerous heights

There is an increased fall damage on the server.

There is also a phenomena, where suddenly out of nowhere you suffer a massive fall damage, which sometimes kills you. This is a bug and there is not much you can do to avoid it, other than avoiding the places where this happened. Think of it like your character just fall. This is one of the reasons, why you can't loose the Ironman Challenge to fall damage.

If you run into this issue, please report it using the link showed [here](#reporting-bugs), with details where the incident happened.

#### Free market

All of the action houses are connected. Horde, Alliance, Neutral, all of them.

#### Cheap rides

Your first riding lessons at level 40 are free of charge

#### Public transport

Some zeppelins and boats change their destinations. Talk to the NPC before boarding to make sure you don't end up somewhere you don't want to!

### Making suggestions

There are some technical limitations that the developers are unwilling to take on, and for a good reason. If your suggestion requires the WoW.exe to be modified, it is an automatic no-no, for it has the potential to make massive unforeseen issues. This is non-negotiable and no amount of pleading will make this change.

#### Suggestions to reset the server

Don't. Just don't.

### Helping the server

The server is free to play but the necessary upkeep is not. Donations are welcome and appreciated, but they are just that, donations. Find more information about this on the [website](https://vanillaplus.org/), under the `Support Project` and `Rewards` menu points.

Bringing positive attention to the server is also a great way to help the project. A good example of this would be raising the attention of like minded individuals, such as creating content on twitch or youtube (see [Hamsterwheel](https://www.youtube.com/channel/UCQkKf5qwYKyJlyhZPbdAVmw)). A bad example would be spamming forums and competitors with links to the server. Committing acts of terror to coerce people to play on the server is also shunned. Please do **NOT** engage in war crimes to make the server more popular.

### Reporting bugs

The official bug reporting tool can be found [here](https://docs.google.com/forms/d/e/1FAIpQLScVN-8EP_yRSnDigBbUPLsw7F0O8Zkom8P3dC7a2tRpLyOebA/viewform). Before reporting please make sure that it is indeed a bug. Your best bet is probably to ask about in the discord first and actually wait for some responses before making the report to avoid wasting the developers time.

Provide as much detail as possible so they will have an easier time recreating the issue. Reports like "I died" is not helping. However a detailed report with screenshots, map locations, character information, etc will allow for quick recognition of an issue.

<p align="center">
  <img src="https://user-images.githubusercontent.com/1638449/150676674-635d9298-4ea9-4d04-8d58-f7adf6c76a41.png">
</p>

## Customisation

*Classic is NOT vanilla.* When looking up information about customising your experience always look for information on the `1.12.1` vanilla client. Forgetting about this is one of the most frequently made mistake on discord.

### Addons

There are some community developed addons that are made specificly for the server, but any addon made for `1.12.1` will work. Some have dependencies that you will need to install so always read the readme file.
You may also want to check the pinned messages of the #addons channel and may ask for help on [Discord](https://discord.com/invite/CfC8PGmg?utm_source=https://github.com/KrekoG/vanillaplus&utm_medium=Connect). If you can't find your addon folder at `<wow folder>\Interface\AddOns`, starting the game successfully will create it for you.

#### Server specific addons:
- [AtlasLoot Enhanced for Vanilla+](https://github.com/hawaiisa/Atlas)
- [BloodlustHelper](https://github.com/KrekoG/BloodlustHelper)
- [pfUI Vanilla Plus](https://github.com/heroclastus09/pfui-vanillaplus)

#### Addons maintained by the community:
- [ag_UnitFrames](https://github.com/KrekoG/ag_UnitFrames)
- [BetterCharacterStats](https://github.com/Borcsa134/BetterCharacterStats)
- [SkelaCustomNameplates](https://github.com/KrekoG/SkelaCustomNameplates)
- [SpecialTalentUI](https://github.com/KrekoG/SpecialTalentUI)
- [WIIIUI](https://github.com/Fiurs-Hearth/WIIIUI)

#### Lists of other resources:
- [decaedent.github.io/wow/](https://decaedent.github.io/wow/vadp.html)
- [Legacy-wow vanilla addons](https://legacy-wow.com/vanilla-addons/)
- [dkpminus vanilla wow addons](https://www.dkpminus.com/wow/addons/expansion/vanilla-wow/) - credit: Chuck
- [Twinstar's github list](https://forum.twinstar.cz/threads/github-list-of-vanilla-addons-1-12-1.123906/) - credit: Thirinena

### Macros

Vanilla macros are harder to write as many beloved features were added to the game in later expansions and some functionalities simply don't exist in vanilla.
But [here](https://forum.nostalrius.org/viewtopic.php?f=38&t=21017) is a great resource to take as an example what one can still achieve with a bit of scripting.

#### ROID macros

credit - Jaredc

Roid Macros is aimed to provide TBC like macros (including conditions!) while abusing Vanilla WoW's Lua API to go even further including things like executing macros from within macros!

https://denniswg.github.io/Roid-Macros/

#### Auto attack macros

[Here](https://forum.elysium-project.org/topic/23521-vanilla-startattack-macro/) is another forum entry with a spammable start attack button that you can combo with other abilities.

#### Mouseover macros

credit - Thirinena
```
You'll need an addon to enable it https://github.com/satan666/LazySpell.
Classic mouseover and bonus scanner are needed for it AFAIK,
so it's the only one you'll have to extract from the lazyspell-master
folder if you're not interested in the others.
Use the slashcommand /cmcast [Spell name here](no brackets)
or the CM:Cast("[Spell name here](without brackets)" function
```

### Other modifications

These are patches that changes the way the game looks. Use them with care, some may not remain always compatible, as they are not maintained by the sever, or the community. To make sure the load order does not break, ensure that the name of the file is later in the alphabetical order than `patch-3.MPQ`. (For example `patch-A.MPQ`)

- [Very Dark Night Mod 1.12.1](https://discord.com/channels/530653671193706496/730518138831241297/893600417064321074) - credit: Wizdom
- [Leeviathan's WoD Character Models](https://model-changing.net/gc/11-leeviathans-wod-character-models/) - credit: Thirinena

<p align="center">
  <img src="https://user-images.githubusercontent.com/1638449/150676642-be78688a-298d-456b-9967-1a19b0ac2b21.png">
</p>

## About

This document is currently maintained by [KrekoG](https://github.com/KrekoG/).

If you find any inaccuracies, grammatical errors or would like to suggest (or even write) additions, please contact me on github or discord.

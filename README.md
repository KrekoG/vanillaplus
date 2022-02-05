<p align="center">
  <img src="https://user-images.githubusercontent.com/1638449/150675419-04fdabdc-e111-4a60-8740-23a42eead1ae.png">
</p>

This is a community made brief guide to help out new players starting on the server.

Contents of this guide:
- [How to play on the server](#how-to-play-on-the-server)
  - [Using the launcher](#using-the-launcher)
  - [Not using the launcher](#not-using-the-launcher)
  - [Updating the game](#updating-the-game)
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
  - [Racials](#racials)
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

### Updating the game

#### Using the launcher

The launcher will check for updates and do the necessary steps automatically.

#### Not using the launcher

If you installed the game manually the game will need to be updated with **every** new patch. To do this:
- Download the [patch](https://vanillaplus.org/uploads/patch-3.mpq) from the website and place it in the `<wow folder>/Data` folder
  - If you are a Mac user, make sure the file extension is capitalised, ending up with `<wow folder>/Data/patch-3.MPQ`
- Remove any previously downloaded cache by deleting the contents of your `<wow folder>/WDB` folder
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
- Add the following lines to the end of your `<wow folder>/WTF/Config.wtf` file (you can open it with notepad for example):

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

![image](https://user-images.githubusercontent.com/1638449/150698918-c7c95bec-7a31-4790-b8eb-2b3222457adc.png)

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

### Racials

<table style="text-align:center;">
  <tr>
    <td rowspan="2">
      <img src="https://user-images.githubusercontent.com/1638449/152647692-d4065a19-8657-48cc-b2c3-b1b82bbf0224.png"><br/>
      <b>Human</b>
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152647658-781b7f5b-88df-4b53-84e9-393233046afa.png"><br/>
      <b>Sword Specialization</b><br/>
      Skill with Swords and Two-Handed Swords increased by 5.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152648050-edacd31b-f69b-4a05-a0b0-9c53c25241a5.png"><br/>
      <b>Mace Specialization</b><br/>
      Skill with Maces and Two-Handed Maces increased by 5
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152648072-f9a93649-3d02-497c-9cc6-f88a5a228d22.png"><br/>
      <b>Diplomacy</b><br/>
      Reputation gains increased by 10%
    </td>
  </tr>
  <tr>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152648109-789f74e6-1828-4a2c-ba11-6c6f5687b2b9.png"><br/>
      <b>Perception</b><br/>
      Dramatically increases stealth detection.<br/>
      <i>Instant cast, 2 min cooldown</i>.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152648255-b29e9ba8-078b-4f4a-a2fa-39aace587873.png"><br/>
      <b>Perseverance</b><br/>
      Removes all Fear, Silence and Movement Impairing effects.<br/>
      <i>Instant cast, 3 min cooldown</i>.
    </td>
    <td>
    </td>
    <td>
    </td>
  </tr>
  <tr>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152647703-43ad4ce9-a12f-45fe-a3f0-2bd92101fff1.png"><br/>
      <b>Dwarf</b>
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152651474-dc3c0aa2-d907-41df-a03b-6e497b0a358a.png"><br/>
      <b>Axe Specialization</b><br/>
      Skill with Axes and Two-handed Axes increased by 5.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152651530-4b5e4082-916e-4e4d-88c9-c7fef997c381.png"><br/>
      <b>Thunderer</b><br/>
      Skill with Maces, Two-handed Maces and Guns increased by 5.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152651545-7b4a2cf1-8e82-4544-a4c1-a051f88e4386.png"><br/>
      <b>Frost Resistance</b><br/>
      Frost resistance increased by 20.
    </td>
    <td>
      <img src=""><br/>
      <b>Metallurgy Specialisation</b><br/>
      Mining and Blacksmithing skill increased by 15.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152651816-926ef333-7fb0-4c46-909f-639d72109d90.png"><br/>
      <b>Stoneform</b><br/>
      While active, grants immunity to Bleed, Poison and Disease effects. In addition, physical damage taken is reduced by 20%. Lasts 15 sec.<br/>
      <i>Instant cast, 5 min cooldown.</i>
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152651838-ff4be474-a733-4fb2-8818-e0bd35107079.png"><br/>
      <b>Find Traesure</b><br/>
      Allows the dwarf to sense nearby treasure, making it appear on the minimap. Lasts until cancelled.
    </td>
    <td>
    </td>
  </tr>
  <tr>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152647717-fb20c109-de6b-473c-92bc-d024c829f25f.png"><br/>
      <b>Night Elf</b>
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652120-d8b84303-69e6-45f1-9505-b6313887b494.png"><br/>
      <b>Moonglaive Specialisation</b><br/>
      Skill with Polearms and One-Handed Swords increased by 5.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652161-ae3ae8fa-8066-475a-9c21-306a93431932.png"><br/>
      <b>Quickness</b><br/>
      Increases your Agility, movement and casting speed by 5%. This does not stack with other movement speed increasing effects.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652182-ba9ebec7-35c9-4695-a635-4da924c8a420.png"><br/>
      <b>Nature resistance</b><br/>
      Nature Resistance increased by 20.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652193-7f91630a-2428-4463-9e48-cb224fbcdc7a.png"><br/>
      <b>Ultravision</b><br/>
      Stealth and invisibility detection increased.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652347-c1354313-0a52-480a-954b-660b29b7b9a0.png"><br/>
      <b>Wisp Spirit</b><br/>
      Transforms into a wisp upon death, increasing speed by 50%.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652418-6810b7fe-e572-436c-9b50-3025169cdf91.png"><br/>
      <b>Shadowmeld</b><br/>
      Activate to slip into the shadows, reducing the chance for enemies to detect your presence. Lasts until cancelled or upon moving. While active, increased your Health and Mana regeneration rate. Night Elf Rogues and Druids are more difficult to detect while stealthed or prowling.<br/>
      <i>Instant cast, 10 sec cooldown.</i>
    </td>
    <td>
    </td>
  </tr>
  <tr>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152647728-e0823e60-38de-4e6e-a14d-019743e69ada.png"><br/>
      <b>Gnome</b>
    </td>
    <td>
      <img src="?"><br/>
      <b>Thirst for Adventure</b><br/>
      Your skill with Fist and Dagger weapons increased by 5 and damage dealt versus Giants increased by 5%.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652460-7df29fb6-636c-494e-8cc4-1c602b1352e3.png"><br/>
      <b>Expansive Mind</b><br/>
      Intelligence increased by 10%.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652347-c1354313-0a52-480a-954b-660b29b7b9a0.png"><br/>
      <b>Arcane Resistance</b><br/>
      Arcane Resistance increased by 20.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652576-198c1369-8a97-4bc4-b54b-53abf79f86e3.png"><br/>
      <b>Engineering Specialization</b><br/>
      Engineering skill increased by 15.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652622-2a9d7b25-bb16-43f6-8336-6e5d82bd2a28.png"><br/>
      <b>Escape Artist</b><br/>
      Escape the effects of any movement speed reduction effect.<br/>
      <i>Instant cast, 1 min cooldown.</i>
    </td>
    <td>
    </td>
    <td>
    </td>
  </tr>
  <tr>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152647735-8eded22e-1e2f-4395-be95-a7b89774a6c9.png"><br/>
      <b>Orc</b>
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152651474-dc3c0aa2-d907-41df-a03b-6e497b0a358a.png"><br/>
      <b>Axe Specialization</b><br/>
      Skill with Axes and Two-Handed Axes increased by 5.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652876-f281b16e-c974-4a60-aa5a-39a64994f82f.png"><br/>
      <b>Command</b><br/>
      Damage dealt by Hunter and Warlock pats increased by 10%.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652860-5d864c1e-8897-4a00-86a1-003d26c41dd7.png"><br/>
      <b>Hardiness</b><br/>
      Chance to resist Stun effects increased by an additional 15%.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652812-980504b1-52b0-436d-beb4-4c3713fdb223.png"><br/>
      <b>Blood Fury</b><br/>
      Increases your chance to get a critical strike with all attacks and spells by 15% for 20 sec but reduces healing effects on you by 25%. <i>Instant cast, 5 min cooldown</i>
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
  </tr>
  <tr>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152647744-0ce405f1-aeaa-43bb-ad10-f2e486196a8f.png"><br/>
      <b>Undead</b>
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152647658-781b7f5b-88df-4b53-84e9-393233046afa.png"><br/>
      <b>Sword Specialization</b><br/>
      Skill with Swords and Two-Handed Swords increased by 5.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652965-b69e1449-9ea8-4614-be6d-41ffa0cb6454.png"><br/>
      <b>Shadow resistance</b><br/>
      Shadow resistance increased by 20.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652980-c8af8797-b418-4704-af5d-b44495b2111e.png"><br/>
      <b>Underwater Breathing</b><br/>
      Underwater Breath lasts 300% longer than normal.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652934-5e816c62-8cf3-48c2-a25d-26f18ce2ec42.png"><br/>
      <b>Cannibalize</b><br/>
      When activated, regenerates 7% of total health every 2 sec for 10 sec. Only works on Humanoid or Undead corpses within 5 yds. Any movement, action, or damage taken while Cannibalizing will cancel the effect.<br/>
      <i>Instant cast, 1 min cooldown</i>
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652989-c9d673f4-5f3c-4cc0-a4f5-12539a24193e.png"><br/>
      <b>Will of the Forsaken</b><br/>
      Provides immunity to charm, Fear, and Sleep while active. May also be used while already affected by Charm, Fear Or Sleep. Lasts 5 sec.<br/>
      <i>Instant cast, 3 min cooldown.</i>
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152653005-925ab2af-5b81-4c95-ba11-27434700e13f.png"><br/>
      <b>Fake Death</b><br/>
      Feign death which may trick enemies into ignoring you. Lasts up to 30 sec. While inside dungeons, all threat is restored upon end of this effect.<br/>
      <i>Instant cast, 5 min cooldown.</i>
    </td>
    <td>
    </td>
  </tr>
  <tr>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152647749-f6bb9e0d-a3c1-45c8-8b7d-69584c60d276.png"><br/>
      <b>Tauren</b>
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152653060-9f0abde7-68fa-4be5-9f72-d7b5425f2c93.png"><br/>
      <b>Pulverize</b><br/>
      Skill with Fists, Maces and Two-Handed Maces increased by 5.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152653120-7f22d6d4-428c-4a97-bd18-05e1f8d3702b.png"><br/>
      <b>Endurance</b><br/>
      Total Health increased by 5%.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152652182-ba9ebec7-35c9-4695-a635-4da924c8a420.png"><br/>
      <b>Nature Resistance</b><br/>
      Nature Resistance increased by 20.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152653075-169227a3-7447-4e63-8b67-5b0f620ca602.png"><br/>
      <b>Cultivation</b><br/>
      Herbalism skill increased by 15.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152653142-0c253f1d-b04b-4f77-92c1-d3155b7cb77f.png"><br/>
      <b>War Stomp</b><br/>
      Stuns up to 5 enemies within 8 yds for 2 sec.<br/>
      <i>Instant cast, 2 min cooldown.</i>
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152653106-f6cc8107-c1a8-40fd-884c-e910bb9eb37e.png"><br/>
      <b>Plainsrunning</b><br/>
      Gradually increases your running speed.<br/>
      Any action or damage taken cancels the effect. Only usable outdoors and out of combat.<br/>
      <i>Instant cast, no cooldown.</i>
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152653219-a1423bed-4c8a-4b39-b34c-10945b8185af.png"><br/>
      <b>Long Reach</b><br/>
      Melee attack range is increased by 2 yds<br/>
      <i>While this in not shown in the Spellbook, it is easily testable in a duel.</i>
    </td>
  </tr>
  <tr>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152647753-aaa081ab-7dcf-4e0e-bccf-a1c0104ddd6d.png"><br/>
      <b>Troll</b>
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152651171-90f5c486-32d7-42c3-a13e-420de3661818.png"><br/>
      <b>Hunting Weapons Specialization</b><br/>
      Skill with Bow and Polearms increased by 5.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152651245-c2b95bdb-1135-4f3b-8673-9877ea7ddabd.png"><br/>
      <b>Light Weapons Specialization</b><br/>
      Skill with One Handed Axes, Daggers and Thworing Weapons increased by 5.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152651191-03067890-3e9d-498c-98f2-a4fc8b0918e8.png"><br/>
      <b>Monster Slaying</b><br/>
      Damage dealt versus Beasts and Dragonkins increased by 5%.
    </td>
    <td>
      <img src="https://user-images.githubusercontent.com/1638449/152651206-83bd8b2e-99b3-435e-954a-8365f42bdd28.png"><br/>
      <b>Regeneration</b><br/>
      Health regeneration rate increased by 20%. 15% of total Health regeneration may continue during combat.
    </td>
    <td colspan="2">
      <img src="https://user-images.githubusercontent.com/1638449/152651274-72725dcb-e3d6-403c-a0c6-f8eb48f1e150.png"><br/>
      <b>Berserking</b><br/>
      Increases your attack speed by 10% to 30%. At full health the speed increase is 10% with a greater effect up to 30% if you are badly hurt when you activate Berserking. Lasts 20 sec.<br/>
      <i>Instant cast, 3 min cooldown.</i>
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
  </tr>
</table>

Partial credit goes to Rafale for making [this](https://docs.google.com/spreadsheets/d/1saPBmoyzwzV1NItwBV73F51GL8DxmDSL9a1YAbetr3Q/) list of racial changes.

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

The talent reset cost has been capped to 5G maximum and it resets every 3 days.

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
- Azshara Crater

To incentivise PVP, you get one mark per hour for queueing. Furthermore you may buy flasks with your marks. When there aren't enough players for the battleground to continue, it closes down, rewarding one of the teams randomly with 3 marks, regardless of the state of the match.

You may join the queue from anywhere, by typing `.wsg`, `.ab` or `.ac`. This summons an invisible npc to talk to you. Beware though, once your battleground is finished, you will get teleported back to place where you joined the queue.

If the losing team is able to drag the match out for more than 10 minutes, they are also awarded a token for the loss.

#### Azshara Crater

Azshara Crater is a vanilla+ made MOBA-styled custom battleground, where the two factions, the Firebird corps (Alliance) and the Operation Rattlesnake (Horde) fight their battles, currently running in **testing mode**. This means there are no quests, side objectives and reputation vendors activated yet, but reputation with new factions and Honor rewards are available.

The pattern of AC seems like Alterac Valley: each team has five towers, General and Warmasters.
Each team starts with 500 Initiative points, the team who gets 1000 Initiative points wins, the team who lost all Initiative points loses the game.

There're few ways to raise your Initiative points and to reduce enemy Initiative points:
By controlling Crystal Depths (Tug-of-War middle point), you reduce your foe's Initiative.
Destroying the enemy tower will reduce his Initiative and despawn one Warmaster per tower.
To gain an Initiative, you should control Temple of Quel'Arkhana points or slay their ancient guardian.

To join a queue, use the `.ac` chat command.

You may use the #azshara-crater-feedback channel to report bugs/suggestions related to the new battleground on the discord server.

#### Getting payed for your merchanary work

You may turn in your Marks of Honors for money rewards at the entrances of the battlegrounds. For example looks for Sentinel Farsong on Alliance side, and Captain Shatterskull on Horde side with your Warsong gulch marks. The rewarded amount scales with your level.

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

#### Half-empty barrels and crates

The drink and food containing barrels and crates have level requirements. They may look empty at first, but if you are high enough level, you'll find what you are looking for.

### Making suggestions

You can make suggestions in the #suggestions channel of the discord server. To make one you must start your message with `!suggest`, for example `!suggest Add Arcane Blast or make Arcane Missiles benefit from 20% increased cast time talent.`. This will show up as a suggestion with others able to vote on it showing how populare your idea is.
![image](https://user-images.githubusercontent.com/1638449/151654432-598d912f-6edf-412d-85c2-e5be8c627364.png)

There are some technical limitations that the developers are unwilling to take on, and for a good reason. If your suggestion requires the WoW.exe to be modified, it is an automatic no-no, for it has the potential to make massive unforeseen issues. This is non-negotiable and no amount of pleading will make this change.

#### Suggestions to reset the server

Don't. Just don't.

### Helping the server

#### Donations

The server is free to play but the necessary upkeep is not. Donations are welcome and appreciated, but they are just that, donations. Find more information about this on the [website](https://vanillaplus.org/), under the `Support Project` and `Rewards` menu points. You may talk to **Landro Longshot** for possible supporter rewards in front of your faction's auction house.

![image](https://user-images.githubusercontent.com/1638449/152032313-47ffd376-1a5c-4fee-a9e6-1cd514a3cf2f.png)

<details>
  <summary>Here are some examples of said possible supporter rewards</summary>

  ##### Ogre's Bum Bag (36 slot)

  ![image](https://user-images.githubusercontent.com/1638449/152030177-72f65337-9ae4-407a-876b-0c292b0dc2c2.png)

  ##### Summonable Caravan Mule (Bank)

  ![image](https://user-images.githubusercontent.com/1638449/152029125-882e1fbc-bc1c-4e98-9ca0-5b1f53b76ac9.png)
</details>

#### Advertising

Bringing positive attention to the server is also a great way to help the project. A good example of this would be raising the attention of like minded individuals, such as creating content on twitch or youtube (see [Hamsterwheel](https://www.youtube.com/channel/UCQkKf5qwYKyJlyhZPbdAVmw)). A bad example would be spamming forums and competitors with links to the server. Committing acts of terror to coerce people to play on the server is also shunned. Please do **NOT** engage in war crimes to make the server more popular.

### Reporting bugs

The official bug reporting tool can be found [here](https://docs.google.com/forms/d/e/1FAIpQLScVN-8EP_yRSnDigBbUPLsw7F0O8Zkom8P3dC7a2tRpLyOebA/viewform). Before reporting please make sure that it is indeed a bug. Your best bet is probably to ask about in the discord first and actually wait for some responses before making the report to avoid wasting the developers time.

Provide as much detail as possible so they will have an easier time recreating the issue. Reports like "I died" is not helping. However a detailed report with screenshots, map locations, character information, etc will allow for quick recognition of an issue.

<p align="center">
  <img src="https://user-images.githubusercontent.com/1638449/150676674-635d9298-4ea9-4d04-8d58-f7adf6c76a41.png">
</p>

## Customisation

*Classic is NOT vanilla.* When looking up information about customising your experience always look for information on the `1.12.1` vanilla client. Forgetting about this is one of the most frequently made mistake on discord.

![image](https://user-images.githubusercontent.com/1638449/150698993-0d243de1-a40d-42df-b379-79aa9096e0be.png)

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

#### How to check that an addon is installed correctly

To check that you have installed it properly, make sure that the structure in place is the following:

`<Wow folder>\Interface\AddOns\<addon_name>\<addon_name>.toc`

If the `.toc` file is not in there, the game will not recognise the addon, and you might need to move the folders about. However if the `.toc` file isn't there, don't just move the `.toc` file, but move the whole folder, as it was originally extracted from the archive file (`.zip`/`.rar`/`.7z`).

Also, if the folder's name is `<addon>-master`, while the `.toc` file is `<addon>.toc`, then remove the `-master` from the folders name.

![image](https://user-images.githubusercontent.com/1638449/151720066-1b6625d6-6841-497c-a730-4f2be180e4a5.png)

### Macros

Vanilla macros are harder to write as many beloved features were added to the game in later expansions and some functionalities simply don't exist in vanilla.
But [here](https://forum.nostalrius.org/viewtopic.php?f=38&t=21017) is a great resource to take as an example what one can still achieve with a bit of scripting.

Another great resouce can be found [here](https://github.com/DBFBlackbull/wow-macros/blob/master/Vanilla%201.12/Warrior-macros.md), credit goes to [DBFBlackbull](https://github.com/DBFBlackbull/) for the nice explanations. While his focuses on warrior macros, reading through his page helps understand how macros function in vanilla.

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

Should you want to help share information from this guide, you may click on the headers and the url in your browser will change. If you copy and paste the new url, the opener of the link will be directed to the selected part right away.

This document is currently maintained by [KrekoG](https://github.com/KrekoG/).

If you find any inaccuracies, grammatical errors or would like to suggest (or even write) additions, please contact me on github or discord.

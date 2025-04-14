# Altoholic_Vanilla

This is my version for Turtle WOW. See the original README below.


This version fixes several bugs, improves some things, and adds a menu tab to show
Raid lockouts and reset times.

If you have several accounts, or cleared your WDB folder, a character might not know
some of the items in the auction/bid lists, which lead to crashes. Now those items
are shown as blank squares and requested from the server for future display.

Character lists are sorted by character level backwards, then name. So your level 60's
are always on top, and your level 1 bank characters are always on bottom.

The new character sort order also fixes the problem that sometimes clicking on a character
made a different character pop up (caused by LUA tables not preserving order).

The quest log messed up after a while, making quests show as header lines.

Reputations and Equipment are now limited to your 10 highest character; this was a problem
if you had more than 10 characters when you had more than 1 account.

Profession skills are shown with their first letter now, so "Jewelcrafting 300" shows as
"J300", not 300, which makes it easier to find a skill.

A new tab shows which characters have raid lockout IDs for which raid.
This includes reset times which are shown when you hover over a raid name in the title,
no more reason to tab out and use the (excellent!) turtle timers.

Added several Turtle specific factions to the factions list.





------------


Altoholic for Vanilla WoW 1.12 - backported from version 2.4.015 originally written by Thaoky

*Please Note:*
- Please use the <a href="https://github.com/Dyaxler/Altoholic_Vanilla/issues">issue tracker</a> to report bugs!

Screenshots:

<img src="https://github.com/Dyaxler/Altoholic_Vanilla/blob/master/Screenshots/Equipment.JPG" alt="Equipment"/>

<img src="https://github.com/Dyaxler/Altoholic_Vanilla/blob/master/Screenshots/Containers.JPG" alt="Containers"/>

<img src="https://github.com/Dyaxler/Altoholic_Vanilla/blob/master/Screenshots/Characters_Tooltips.JPG" alt="Tooltips"/>

Features:

- Language supported: English and French. Although it's not fully localized for frFR, it does run well on French clients (my guildmates made sure of this :D). More languages will come soon, I'm using the LibBabble libraries more & more.


- Account-wide data summary:
	- Characters' talents: only a summary, not a full buid, I may implement this later on if there's demand.
	- Money, /played, rest xp for each character, subtotals by realm, and grandtotals for the account.
	- Bag usage: see at a glance which characters should get bigger bags (bag size, free slots and types included)
	- Characters' skills: skill summary on one screen, namely the 2 main professions + the 3 secondary skills as well as riding. I may add more if there's demand.
	- Reputations: a list of all the reputations of the current realm's characters. This screen will get some love in the future, but it's perfectly functional. You can see at a glance if all your alts are at least honored with Honor Hold if you want to get the new 2.4 blue PVP set.

- View containers (bags, bank, keyring) of all alts, on all realms.

- Guild banks : You have 10 alts in 10 different guilds on the same server, all of them with access to a guild bank ?
Not a problem, you can see them all here.

- E-mail: allows you to see which alts have mail without having to reconnect them. The addon will tell you when mail is about to expire on a character. Threshold configurable (up to 15 days). Multiple realm support as well. Mails sent to a known alt (one you've logged on at least once) will be visible in the addon.

- Equipment: See the equipment of the current realm's alts in one screen. Very useful when purchasing stuff for your alts at the AH.

- Options: the option screen is still a bit minimal, I'll add more options along the way depending on user requests.

- Search: the most important feature of the addon, it uses an AH-like frame to display search results. You can either search bags on the current realm, on all realms, or a loot table.
The loot table is a table based on AtlasLoot 4.04 which contains only item id's, and therefore keeps memory usage minimal.
As an indicator, with 10 alts (+bank) + guild bank + loot table, the addon only takes 2.3 mb of memory. The addon has gained weight since the integration of some libraries, but this will ensure support for multiple languages in the future. I expect to support deDE soon.

The Search menu allows you to find items based on their name (even partial), level, type or rarity, almost like at the AH.

How to Install the addon
========================

Make sure you unzip the addon using "Extract Here" instead of "Extract to Altoholic v2.x.yyy", otherwise the resulting directory will contain a space that will prevent the addon from being visible in WoW's addon list.

Using command-line searches
===========================

Type: /alto search <item>
ex: 
/alto search cloth
/alto search primal
...

A maximum of two words is allowed after the command, so you could type:
/alto search primal mana 		... and get only those primals in the search results.
This should cover most of the searches you can do via the command line, if you actually need something more complicated, please use the UI.

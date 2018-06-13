Civil Auras Changelog
=======
# 1.7.4.1b (Hotfix)
* Added the "CanNotUse" AIFlag to all CA skills. The AI should now ignore these skills if your character has lost control (polymorphed, charmed, etc).

# 1.7.4.1
* Minor Script Updates
	* Refactored Barter sharing script. Should work better across the board.
	* Modified "Remove Aura Statuses" debug command to apply to the whole party. This is now a host-only command.
	* Rewrote host-checking script.

# 1.7.4.0
* Added some checks/fixes for when your stats change and you lose the civil ability level required to cast an aura.
	* By default, you'll get a status message that aura requirements were lost, and your aura will be removed (and all related databases reset).
	* When you regain the required stats, your aura skill will "refresh" (normally skills are unmemorized when you lose the requirements), and you'll get a status message that your aura requirements were regained.
* Added a passive "fix" when attempting to learn an aura skill after it was unmemorized. The skill should refresh, but you may need to open up your memorization window and drag it back down to your hotbar to get the skill to work.
* Added the ability to disable status messages in the CA Settings Menu (under Aura Settings).

# 1.7.3.0
* Added LeaderLib support (dependency-free, a.k.a. optional).
	* If LeaderLib is installed, Civil Auras will register its settings to the LeaderLib "Mod Menu". Otherwise, the settings book will spawn as normal.
* Auto-Sneaking update. 
	* Stealth Aura can now toggle off sneaking for controlled characters. This is configurable in the settings menu.

# 1.7.2.0
* Updated to the latest hotfix.
* Story Script Refactoring
	* Moved mod updating code to a new script (loaded last).
		* Uses a slightly different database now for potential cross-mod interaction.

# 1.7.1.2
* Updated to the latest official patch.
	
# 1.7.1.1 (Minor Revision)
* Minor Hotfix
	* Fixed CA settings books not spawning on a new game - this was removed unintentionally when refactoring things in 1.7.1 (the books still spawned on loading a save).

# 1.7.1.0
* Bug Fixes
	* Fixed bonuses not applying under some circumstances (apply timers not clearing properly).
	* Fixed Pep Talk not applying bonuses correctly (dumb typo).
* Aura System
	* Auras and aura bonuses now refresh quietly if the relevant stats change. 
* CA Settings Book
	* New command to display debug messages.
		* Will display these messages in the combat log as well (if enabled), on fresh campaigns.
	* Added a mod version display in the main menu.
	* Labeled debug commands with handy tags.
	* Tweaked the "Remove Aura Statuses" command to also clear related databases. Use this command if something seems funky on existing saves.

# 1.7.0.0
* New Persuasion Aura
	* Works as an eventual upgrade to Pep Talk, for applying your persuasion bonus to allies.
* New Icons
	* Added new icons for all the CA abilities and statuses.
* New Ability Point Bonus System
	* "Invisible" statuses are now used to apply bonus points - these should be exploit-free and generally safer (bonuses from statuses aren't turned into real points at the respec mirror).
	* Bonus points from previous CA versions ("Legacy" versions) should automatically be updated to the new system - your auras may be toggled off on loading an existing save. This is intended in order to remove the previous bonus points.
* CA Settings Book
	* New debug command for removing CA statuses from user-owned characters, if for some reason they become "stuck" (a common DOS2 bug). Use this if a status suddenly doesn't toggle off.

# 1.6.5.0
* CA Settings Book
	* Made most debug commands host-only commands.
	* Remove gold value from the skillbooks spawned by the debug command (host only).
* Mirror Exploit/Bugs
	* Added an additional check for barter when interacting with the mirror.

# 1.6.4.0
* Quick update in response to the latest game patch.

# 1.6.2.0
* Quick fix for a double config book spawning in a new game.

# 1.6.1.0
* Quick update to fix the "Remove Bonus Points" command.
	* Made it remove equipment first before checking the bonus points. The equipment is then re-equipped once done.

# 1.6.0.0
* New CA Settings Book
	* Aura Settings
		* Enable/Disable Auto-Sneak when affected by the Stealth Aura (on the first apply).
			* When enabled, when the "Stealthy" status first hits a controlled character, they'll auto-sneak. Characters controlled by other users should be ignored.
	* Barter Settings
		* Enable/Disable barter sharing.
			* Allows you to blacklist users from sharing bartering bonuses.
				* For instance, turning this on in singleplayer will effectively disable it. Using it in multiplayer will disable it for the individual user and all their assigned characters.
	* Debug Commands
		* Add all CA skillbooks to inventory.
			* Obviously you're free to cheat to your heart's content, but consider using this as a last resort if, for some reason, the vendors don't appear to be selling the books.
		* Refresh CA skills.
			* This will add/remove CA skills you've learned. This is a workaround for a bug where your learned skills get removed, yet the game still thinks you've memorized them, so the skillbooks won't work.
		* Force vendor refresh.
			* This forces a reset in my trader item generation system. Normally this reset occurs on level up, during natural trader generation, or upon entering a new level.
		* Refresh databases.
			* This is an internal command I use to force previous saves to update certain databases when upgrading to a newer version. You can manually force a refresh with this command.
		* Display/hide flag changes.
			* This is a way to display flag changes above a character's head. Give it a shot if you're curious how the dialog menu works.
		* Remove all bonus points from character.
			* This is a way to reset your bonus civil point values, placing you back at base civil point values. Use this if you messed the game up somehow and your aura bonus points became permanent. Unequip your stat increasing equipment pieces first, if you don't want to mess something up!
* Tweaked some scripts to hopefully be correct (singleplayer/multiplayer distinction with the barter sharing).
* Removed barter sharing messages.
	* Will possibly be added back in later, with an opt-in setting, and adjustable appearance rates.

# 1.5.1.0
* Pep Talk tweaks:
	* Added two new effects.
	* Reduced cooldown (5 -> 3)
	* Fixed Motivated's effect positioning.
* Fixed more mirror/respec exploits.

# 1.5.0.0
* (Hopefully) fixed an unlimited talent exploit - talentbooks now only grant a talent to a specific character once. Respecing won't bypass this.
* Restructured trader item generation to only spawn one book (per skill) at a time - Players usually only need one specific book per character anyway.
* Bartering bonuses and trade generation are now properly applied when requesting trade through dialog.
* Trade generation now refreshes on level up.
* Pep Talk memorization requirements reduced to 3 persuasion (from 5).

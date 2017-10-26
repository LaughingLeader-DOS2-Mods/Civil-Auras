Civil Auras Changelog
=======
# 1.6.4
* Quick update in response to the latest game patch.

# 1.6.2
* Quick fix for a double config book spawning in a new game.

# 1.6.1
* Quick update to fix the "Remove Bonus Points" command.
	* Made it remove equipment first before checking the bonus points. The equipment is then re-equipped once done.

# 1.6.0
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

# 1.5.1
* Pep Talk tweaks:
	* Added two new effects.
	* Reduced cooldown (5 -> 3)
	* Fixed Motivated's effect positioning.
* Fixed more mirror/respec exploits.

# 1.5.0
* (Hopefully) fixed an unlimited talent exploit - talentbooks now only grant a talent to a specific character once. Respecing won't bypass this.
* Restructured trader item generation to only spawn one book (per skill) at a time - Players usually only need one specific book per character anyway.
* Bartering bonuses and trade generation are now properly applied when requesting trade through dialog.
* Trade generation now refreshes on level up.
* Pep Talk memorization requirements reduced to 3 persuasion (from 5).
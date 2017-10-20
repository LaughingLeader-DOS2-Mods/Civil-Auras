Civil Auras Changelog
=======
# 1.6.0
* New CA Settings Book
	* Contains the follow menus:
		* Aura Settings
			* Currently just used to enable/disable auto-sneak with the Stealth Aura.
		* Barter Settings
			* Allows you to blacklist users from sharing bartering bonuses. For instance, turning this on in singleplayer will effectively disable it. Using it in multiplayer will disable it for the individual user and all their assigned characters.
		* Debug Commands
			* Contains many useful commands, such as refreshing the vendor item generation system, refreshing your CA skills (if one happens to disappear), spawning the skillbooks, and more.
			* Also includes a command to reset bonus points back to their base values. These functions ignore equipment bonuses (whether I want them to or not).

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
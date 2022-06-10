# Overview

Have you ever wondered what happened to the former leaders of your subject after you integrated them? Or perhaps where that primitive leader went after you annexed their planet? Wonder no more! With this mod you will be prompted to choose what to do with the now-unemployed leaders whenever you integrate a subject, conquer a primitive planet, "allow" primitives to join you via covert infiltration, or convert then via a colossus weapon.

Demoted rulers you acquire through integration/conquest/etc. will (in most cases) preserve their existing ruler traits in case they somehow become the ruler of your empire. Rulers demoted for any reason such as being integrated or even losing an election benefit by gaining the same former ruler traits. They may not have won the hearts and minds of voters, but they still rose to the occasion and developed new skills. This will applies when being demoted from ruler for any reason, such as gameplay from another mod.

Regular (non-machine and non-hive) empires can retain leaders from an integrated Machine Intelligence subject if they have full AI rights. The leaders in a Machine Intelligence have enough capacity to act as independent agents, even if the rest of the Pops don't.

Scientists and Admirals are automatically assigned back to their per-integration roles, if they were commanding a science ship or fleet. Notably, if you play with "pause-on-event" the science vessels will then continue their assigned orders after the leader is reassigned for command.

# Changes

A lot of code has gone into figuring out what leaders you can choose to keep based on what kind of country you are playing, what ethics it has, what kinds of assimilation or necrophage might be available. All of that boils down to an event screen that appears when you have integrated a subject or conquered a primitive planet, or a second event when you have infiltrated a primitive planet.

These event present you with a few choices about what you can do with the leaders from the now-defunct subject/primitives. It will show a few different options depending on what is available to you. For example, genocidal empires can only keep leaders that are of their own species and necrophage empires have the option to necrophage leaders. There's a special secret bonus for some kinds of leaders - see if you can figure out what it is.

This mod was designed to be played with the default restrictions on ascension paths - mainly that your empire would normally not have more than one assimilation type available to it. However, it is coded in such a way that if you have multiple assimilation types available, any of the "assimilate" button options invokes the same follow-up code. Each integrated leader (and their species) in a regular (non-machine, non-hive empires) are assigned the first assimilation type that they qualify for in this order: synthetic, then cybernetic, then psionic, then deassimilation.  If you are using my machine deassimilation mod, that type is checked first (before synthetic assimilation).

Finally, this mod adds some special traits (and a special name affix) for demoted former rulers and heirs.  Their names will be followed by brown text indicating that they are the "Former Ruler/Heir of the <Country Name>" and they will gain a special trait depending on their former empire and new leadership role.

## Compatibility

Built for Stellaris version 3.3 "Libra."  Not compatible with achievements.

This mod is designed to understand the species types, ethics, civics, authorities, governments, and origins that are built-in to Stellaris. The features of this mod are implemented primarily through brand new events and scripting, meaning that it should not directly conflict with most other mods. However, you could end up with odd behavior if you play with mods that significantly alter the default gameplay - for example, adding a new homicidal species (without the mod providing an update to the `is_homicidal` trigger). Mods that add or modify civics should generally work but this mod may offer decisions that do not make the most sense for the role-play of new civics.

### Required Mods

[Primitive Conquest Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2488154830) adds a necessary extension point (dev speak for "it adds something I need") for detecting when the primitive infiltration mission completes. If you don't install it, then this mod won't be able to offer you a choice when infiltration is complete.

### Recommended Companion Mods

* [Leader Traits: All Eligible Species Traits](https://steamcommunity.com/sharedfiles/filedetails/?id=2499031295) will ensure your leaders get all their species-based traits when being assimilated (such as Psionic or Erudite).
* [Leader Traits: Enhanced Randomisation](https://steamcommunity.com/sharedfiles/filedetails/?id=2553806265) improves leader trait randomisation (primarily from level up, but not exclusively) and toggles traits from the biological version to machine traits (and back) if a leader becomes a robot and/or returns to a biological form.
* [Deassimilate Machines](https://steamcommunity.com/sharedfiles/filedetails/?id=2553812372) allows you to "deassimilate" machine Pops into robots. This is available to any non-machine, non-hive empire that has the Positronic AI technology and doesn't outright ban Artificial Intelligence. Specifically allows (with this mod) for machine deassimilation as a "leadership disposition" choice for integrated machine empire subjects (and if you also have Leader Traits: All Eligible Species Traits, the leaders are converted to have synth leader traits if you have the right technology).
* [corsairmarks's Leader Traits MOD Chinese patch](https://steamcommunity.com/sharedfiles/filedetails/?id=2558494770) by Hua Zhang - Chinese localisation

You might wonder - why are these separate mods? They override default gameplay options, so I thought it best to give players the choice on whether they want the original version or the reimagined version. Leader Traits: Enhanced Randomisation and Machine Deassimilation were developed alongside this mod.

### When to Install

This mod can be safely added to your savegame after the game has started. If you remove it, you will lose access to the custom "former ruler/heir" traits and the espionage bonus that is one of the choices upon successfully infiltrating primitives. Stellaris is fairly forgiving in situations like this - it's likely that error logs would be generated and the game would otherwise ignore the missing content. Back up your savegame before trying to remove a mod.

### Additional Mods with Gameplay Interaction

* [Eldanær Stellar Authority](https://steamcommunity.com/sharedfiles/filedetails/?id=2496360535) - if you integrate them, their former ruler and heir are guaranteed to be Governors
* [Special Leadership Privileges for Battle Thralls and Bio-Trophies](https://steamcommunity.com/sharedfiles/filedetails/?id=2496357447) - interacts with special leadership privileges: a) you will keep military leaders from species set to Battle Thralls but also Full Military Service, b) respects species flagged for allowing military leaders despite the empire being xenophobic and/or a necrophage, and c) allows Rogue Servitors to choose to retain organic leaders as Organic Advisors

## Known Issues

### Stellaris Bugs

Demoted rulers with very long names that also contain a period `.` may cause error logs when the Leader screen is open.  It seems related to the font re-coloring in the "former ruler" name affix.  Don't leave the Leader window open for long periods of time or you will generate a very large error log file.

When cloning a leader and changing them from a species class without gender to a species class with gender (or vice versa) the Leader screen interface breaks. The Leader screen does not hide the replaced leader or correctly show their replacement until the player manually recruits a new leader.

## Changelog

* 1.0.0 Initial version
* 1.0.1 Add thumbnail
* 1.0.2 Support Decree: Honored Protectors in Full Military Service for Battle Thralls (now Special Leadership Privileges for Battle Thralls and Bio-Trophies)
* 1.1.0 Auto-Assign and UI Enhancements
    * Automatically reassign Scientists and Admirals from integrated subjects back to their previous fleet command roles
    * Improve some `allow` triggers to be more lenient (most notably the Send them for assignment/"Keep as many as possible")
    * Refactor choices into more `option`s, which allows me to present icons for many of the choices based on civic/authority/ascension perk
    * Demoted rulers/heirs are forced out of their office rather than cloned - mainly this means they will preserve their existing ruler traits when moving to your empire
    * Demoted rulers/heirs will be a somewhat more biased towards being Governors (the built-in Stellaris default if their gov't doesn't specify and they don't have a pre-ruler class)
    * Some demoted rulers/heirs will still be cloned if their demoted class isn't one normally allowed to be a ruler for the government which they previously lead (e.g. Star Empires are run by military leaders) and they don't have a pre-ruler class
    * Code improvement: use a hidden country to store the leaders in limbo (and variables), rather than the global event country
    * Code improvement: cloned leaders will get a random amount of XP instead of having to start again from 0
* 1.1.1 Fix subtle bug with allowing cybernetic/synthetic assimilation for leaders
* 1.2.0 Any demoted ruler (such as the loser of an election) now benefits from a demoted ruler trait
    * Fix a bug where gestalt ruler traits weren't removed upon subject integration
* 1.2.1 Fix scoping error with flag cleanup
* 2.0.0 Update for compatibility with Stellaris 3.1 "Lem"
    * Use army flags instead of hacky variables
    * Support Origin: Necrophage for hive minds
    * Support tradition changes
    * Remove random XP for cloned leaders - we can now copy the exact amount
    * Clean up variable code that can now be done much more simply
* 2.0.1 Support both necrophage unity traditions
* 3.0.0 Update for compatibility with Stellaris 3.2 "Herbert"
    * Ensure necrophaged (and otherwise changed) leaders match the gender of their new species ("Gender Nonbinary Leaders" disables this change)
    * Integrates with "Special Leadership Privileges for Battle Thralls and Bio-Trophies" and "Gender Nonbinary Leaders" to avoid duplicate cloning
    * If using a colossus weapon on a primitive empire that results in the transfer of control of their planet to your empire, you can choose what happens to the leaders
    * Supports these colossus weapons by default: Nanobot Diffuser, Deluge Machine, Necrophagic Spore Diffuser (from Eldanær Stellar Authority)
* 3.1.0 Allow Rogue Servitors to choose to keep organic leaders as advisors when "Special Leadership Privileges for Battle Thralls and Bio-Trophies" is also installed
* 4.0.0 Update for compatibility with Stellaris 3.3 "Libra" - Zombies are not smart enough to be leaders
* 4.0.1 Remove invalid `modification = no` from leader traits
* 4.1.0 "Former ruler" traits no longer give admin cap, instead they grant edict fund
* 5.0.0 Update for Stellaris version 3.4 "Cepheus"
    * Use memory optimization feature for effects and triggers
    * Use `country_base_` modifiers to generate resources from leaders (previous modifier was removed)
    * Use new special bracket syntax when setting names (unable to get the heir's title for Imperial authorities, currently)
    * `SALVAGER` and `SHROUDWALKER` species classes do not use gender
    * Update code to account for hired (mercenary) fleets
* 5.1.0 Allow empires that do not explicitly outlaw artificial intelligence to retain robotic leaders
* 5.2.0 Add a dummy `gov_bureaucratic_autocracy` to stop spamming the error log when Eldanær Stellar Authority is not installed

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/keep_leaders_from_integrated_subjects)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property. That will ensure the game can see the files, and also that CWTools will parse them. Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.
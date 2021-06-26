# Overview

Have you ever wondered what happened to the former leaders of your subject after you integrated them?  Or perhaps where those primitive leaders went after you annexed their planet?  Wonder no more!  With this mod you will be prompted to choose what to do with the now-unemployed leaders whenever you integrate a subject, conquer a primitive planet, or "allow" primitives to join you via covert infiltration.

# Changes

## Compatibility

This mod is designed to understand the species types, ethics, civics, authorities, governments, and origins that are built-in to Stellaris.  The features of this mod are implemented primarily through brand new events and scripting, meaning that it should not directly conflict with most other mods.  However, you could end up with odd behavior if you play with mods that significantly alter the default gameplay - for example, adding a new homicidal species (without the mod providing an update with `is_homicidal`).  Mods that add or modify civics should generally work but this mod may offer decisions that do not make the most sense for the role-play of new civics.

### Required Dependencies

This mod requires the use of my mod [Enable All Eligible Species Traits for Leaders](https://steamcommunity.com/sharedfiles/filedetails/?id=2499031295). This dependency ensures your leaders get all their species-based traits when being assimilated.

### Post-Game Start

This mod can be safely added or removed from your save game after the game has started.  It is implemented entirely through custom events (and custom triggers). If you remove it, your game will work normally.

### Mods With Gameplay Interaction

* [Eldanær Stellar Authority](https://steamcommunity.com/sharedfiles/filedetails/?id=2496360535) - if you integrate them, their former ruler and heir are guaranteed to be Governors
* [Full Military Service for Battle Thralls](https://steamcommunity.com/sharedfiles/filedetails/?id=2496357447) - you will keep military leaders from species set to Battle Thralls but also Full Military Service, and this mod also respects species flagged for allowing military leaders despite the empire being xenophobic and/or a necrophage

## Known Issues

This mod supports features from several of my other mods.  If you are playing without [Eldanær Stellar Authority](https://steamcommunity.com/sharedfiles/filedetails/?id=2496360535) installed, you will get an error log noting a government type doesn't exist:

```
[11:31:50][trigger_impl.cpp:5664]: Invalid government type [gov_bureaucratic_autocracy]!  file:  file: events/keep_leaders_events.txt line: 163 line: 1
```

This error will not affect the functioning of this mod - all built-in government types are handled before the custom one.

## Changelog

* 1.0.0 Initial version

## Source Code

[Hosted on GitHub](https://github.com/corsairmarks/keep_leaders_from_integrated_subjects)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.


Ideas:

special leader traits?
-> generate extra admin cap? hive, mach, serv, assim - gov; swarm, term - admiral; research AI - scientist

TODO: can syth empires integrate machine pops?
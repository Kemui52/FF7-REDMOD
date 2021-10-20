# FF7 Red Mod

A mod for the PS1 version of FF7 that focuses on Red XIII and macro gameplay. Red replaces Cloud in all field maps, the Transform limit break from Cait Sith's slots is available as a selectable limit, and as a bonus, a couple field maps have a quaint rampage mode. Can be played on Disc 3 from a premade save (mostly complete) or a new game from Disc 1 (in progress).

##Progress?

**Disc 1**

Up to Air Buster fight (slums church not started).

**Disc 3**

All areas are accessable from premade save except Gaia's Cliff and the final dungeon.

## How to Play

1) Use xdelta from the Releases section to apply a patch to the matching US bin/cue version of FF7.

(Alternatively, you can add the all caps directory folders to an extracted FF7 filesystem and build it with PSXImager. Just remember to run "fixup" from ff7tools to allegedly fix the LBA offsets.)

2) Open the Cheat Engine table in the !misc folder, say 'no' to the LUA script (unless you want the auto-size buff on), and attach it to your emulator. If playing solo, lock "Party Leader (Field)" to 00 and lock "Second Member" to who you're playing as. This is mandatory to stop the game from mixing up who to display between the field and world map. This could break the world map without Cloud listed as leader, while the second member address makes sure certain field scripts heal the correct character.

(Addresses are offset from the start of PS1 RAM, so if you have a pointer to it for another emulator, you can drag and drop the addresses onto that pointer)

3) If playing Disc 3, use the memory card save in the !misc folder. If playing Disc 1, start a new game. You can use the Black Chocobo save editor to transfer the Disc 3 save to another memory card file if you need to.

## What's New?

The Transform limit break has been added to...

Vincent's limit break forms are controllable, but you can only attack with the one limit attack or a magic attack. It is recommended to use the new Limit materia for unlimited limit breaks.

Some new materia! [Limit] for limitless limit breaks, ...

Mini spell has 100% hit rate and lowers magic attack power. As such, Cornucopia is changed to only cure Mini and raises attack back up. (Actually, it always raises attack even if it fails, but why would you exploit this when I give you better ways to buff your attack?)

Red XIII is controllable in the Round Square ride instead of Cloud. Tail wags!

Temple of the Ancients can be re-explored on Disc 3.

Ho-Chu has been added to the end of the Ancient Forest as a miniboss.

And more I'm forgetting.

## Known Issues

Round Square was redesigned before I came up with the Second Member code trick, so I'm gonna have to wrack my brain over how to account for both a solo and full party.

There's more I forgot here, too. P:

### How to Convert CE Table Address to GameShark

The CE table's codes can easily be converted to GameShark. Right-click the pSX 1.13 RAM Pointer (or whichever you're using) and choose "Browse this memory region". In the bottom section, right-click the upper-left-most byte and choose "Show relative addresses". Now, you can "Browse this memory region" of any address you want and use the shown offset as a GameShark or Xplorer code. Note that battle-specific codes are only valid when in battle and may cause glitchiness in the field.

Example: Party Leader (Field) is `3009D391 00XX`, Second Member is `3009D392 00XX`, and Third Member is `3009D393 00XX`.)
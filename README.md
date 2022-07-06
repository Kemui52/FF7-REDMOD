# FF7 Red Mod

A mod for the PS1 version of FF7 that focuses on Red XIII and macro-themed gameplay. Travel through maps as Red instead of Cloud, and make use of size-changing powers in battle. Use overpowered equipment on Disc 3 from a premade save (mostly complete) or start a new game from Disc 1 (in progress) to tackle a slightly challenging solo run of the original game sequences.

## Current Progress

**Disc 1:** Up to Air Buster fight (slums church not started).

**Disc 3:** All areas that are accessible from the premade save are complete, except Gaia's Cliff and the final dungeon.

## How to Play

1) Use xdelta from the Releases section to apply a patch to the matching US bin/cue version of FF7. The patch is not as up to date as the source files, but is much simpler to install.

(Alternatively, you can add the all caps directory folders to an extracted FF7 filesystem and build it with PSXImager. Just remember to run "fixup" from ff7tools to allegedly fix the LBA offsets.)

2) Open the Cheat Engine table in the `!misc` folder, say 'no' to the LUA script (unless you want the auto-size buff on), and attach it to your emulator. If playing solo, lock "Party Leader (Field)" to 00 and lock "Second Member" to who you're playing as. This is mandatory to stop the game from mixing up who to display between the field and world map. This could break the world map without Cloud listed as leader, while the second member address makes sure certain field scripts heal the correct character.

(Addresses are offset from the start of PS1 RAM, so if you have a pointer to it for another emulator, you can drag and drop the addresses onto that pointer)

3) If playing Disc 3, use the memory card save in the `!misc` folder. If playing Disc 1, start a new game. You can use the Black Chocobo save editor to transfer the Disc 3 save to another memory card file if you need to.

## What's Changed?

The Transform limit break has been added to Red XIII, Aeris, Yuffie, and Cait Sith. The limit breaks are tricky to reorganize, so they have been changed up to mitigate any glitches due to inserting the new ability. This means Limit Level 4 is non-functional, but instead some levels have three limit breaks to choose from!

Vincent's Galian Beast is controllable, but you can only attack with the one limit attack or a magic attack. It is recommended to use the new Limit materia for unlimited limit breaks. The other forms haven't been attempted yet and the game might not allow me to.

Some new materia! [Limit] grants limitless limit breaks, while [Flash], [4x Cut], and [Throw] have been added as individual materia.

Mini spell has 100% hit rate and lowers magic attack power. As such, Cornucopia is changed to only cure Mini and raises attack back up. (Actually, it always raises attack even if it fails, but why would you exploit this when I give you better ways to buff your attack?)

Red XIII is controllable in the Round Square ride instead of Cloud. Tail wags! (My new party leader fix conflicts with this, though, so I'll have to redo this)

Temple of the Ancients can be re-explored on Disc 3 and its dragon can be re-fought.

Ho-Chu has been added to the end of the Ancient Forest as a miniboss.

And more I'm forgetting.

## Known Issues

The tunnel after the first bombing mission crashes randomly for some reason. Still trying to debug it.

The lighting on certain characters is wonky because Red XIII has more model parts than expected. I try to mitigate it by hiding parts of unused models, but it is not always possible. Sometimes, Red himself has the wonky lighting.

Still have Cloud on the world map. Cannot be changed until someone wants to make a program for converting model and animation formats.

Cait Sith's Slots limit break is broken due to the game being very picky about the order of limits. It won't crash as is, but please just stick to his Limit Level 1.

Round Square was redesigned before I came up with the Second Member code trick, so I'm gonna have to wrack my brain over how to account for both a solo and full party.

There's more I forgot here, too. P:

## How to Convert CE Table Address to GameShark

The CE table's codes can easily be converted to GameShark or Xplorer. Right-click the pSX 1.13 RAM Pointer (or whichever you're using) and choose "Browse this memory region". In the bottom section, right-click the upper-left-most byte and choose "Show relative addresses". Now, you can "Browse this memory region" of any address you want and use the shown offset as a GameShark or Xplorer code. Note that battle-specific codes are only valid when in battle and may cause glitchiness in the field.

Example: Party Leader (Field) is `3009D391 00XX`, Second Member is `3009D392 00XX`, and Third Member is `3009D393 00XX`.)
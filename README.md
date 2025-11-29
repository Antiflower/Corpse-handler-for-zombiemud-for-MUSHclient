# Combat Handler + Buff tracker
This contains a corpse handler plugin for use in zombiemud via MUSHclient. Plugin created with the help of Claude AI

Download the plugin
Go to File -> plugins -> add
navigate to the folder containing the .XML file for the Corpse Handler plugin and select it

use the command: corpsemode <Mode> to change modes


NOTE: ALL MODES WILL ATTEMPT TO PUT NOEQ IN BAG AT EXECUTION UNLESS OTHERWISE STATED, SOME MODES WILL ATTEMPT TO GIVE NOEQ TO RANGER PET OR MULE BY NAME, PLEASE UPDATE THE PLUGIN WITH YOUR PET OR MULE'S NAME

Current modes: 

tin(tins corpse, gets can, eats can)

collect: gets corpse, puts corpse in a carriage

sdrain: uses the samurai command sdrain on a corpse

totem: uses the death knight skill vile totem at a corpse(if a totem exists in the room the script will default to the tin command to destroy the corpse, this requires a tinning kit, but you do not need to train 
tinning to tin, only train tinning if you want to actually get cans to eat from the corpse)

ranger: gives all to kevin(you can open the file in an edit and search kevin to replace the name with your own ranger pet's), and say eat all to have ranger pet eat corpses, you can edit this to use beast speech at eat all by scrolling to the ranger section and just replacing the say portion with use beast at

troll: gives all to ranger pet(name change needed), gets the corpse to your inventory so you can eat it later.

archer: tins corpse, gets can, eats can, puts noeq in bag, and puts all arrow in quiver.

none: Does nothing with corpses or loot(for parties where someone else needs to corpse)

This plugin also tracks combat needs such as vulnerability timers, and auto deletes timers when the target dies so you don't spawn party with vulns dropping on dead creatures, otherwise it will announce the vuln has dropped after 25 seconds.

In addition it will also keep track of rounds and announce how many rounds a combat took upon the death of your target, this is in the form of a client note so only you see it.


Combined combat management plugin for ZombieMUD.

VULNERABILITY TRACKING:
- Tracks all 9 vulnerability spell types
- Auto-announces "Vuln Up" to party when cast
- Auto-announces "Vuln Down" after 27 seconds
- Cancels timers automatically on creature death

ROUND COUNTER:
- Tracks combat rounds from "NEW ROUND" messages
- Displays total rounds when combat ends
- Auto-resets on creature death

CORPSE HANDLING:
- Multiple modes: tin, drain, totem, collect, ranger, troll, archer, off
- Automatic corpse processing on creature death
- Totem mode with fallback to tinning if totem exists
- Archer mode includes quiver storage for arrows/bolts
- Ignores troll regeneration mobs (flesh pieces)

Commands:
  corpsemode [mode]  - Set corpse handling mode
                       Valid: tin, drain, totem, collect, ranger, troll, archer, off

Vulnerability spells tracked:
  - Physical (afflictus corpus)
  - Fire (ardens amictus)
  - Cold (aufero fervens)
  - Electric (fulmen infractus)
  - Psionic (ignavus animus)
  - Asphyx (infirmus respiro)
  - Acid (macilentus corium)
  - Poison (macula valetudo)
  - Magic (magus foramen)

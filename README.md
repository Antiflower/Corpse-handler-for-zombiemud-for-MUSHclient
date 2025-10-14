# Corpse-handler-for-zombiemud-for-MUSHclient
This contains a corpse handler plugin for use in zombiemud via MUSHclient. Plugin created with the help of Claude AI

Download the plugin
Go to File -> plugins -> add
navigate to the folder containing the .XML file for the Corpse Handler plugin and select it

use the command: corpsemode <Mode> to change modes


NOTE: ALL MODES WILL ATTEMPT TO PUT NOEQ IN BAG AT EXECUTION.

Current modes: 

tin(tins corpse, gets can, eats can)

collect: gets corpse, puts corpse in a carriage

sdrain: uses the samurai command sdrain on a corpse

totem: uses the death knight skill vile totem at a corpse(if a totem exists in the room the script will default to the tin command to destroy the corpse, this requires a tinning kit, but you do not need to train 
tinning to tin, only train tinning if you want to actually get cans to eat from the corpse)

none: Does nothing with corpses or loot(for parties where someone else needs to corpse)


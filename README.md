# Enchant the Missile Launchers (Ranged Weapon Tweak)

Author: Dee

Beamdog forum <https://forums.beamdog.com/discussion/58374/enchant-the-missile-launchers-ranged-weapon-tweak>

Original Post:

-----

In the tabletop version of AD&D, magical ranged weapons bestow their full enchantment value on any ammunition that is used with them. 
In the Baldur's Gate series, that behavior wasn't possible; when you equip a nonmagical arrow, the engine didn't know how to see the
launcher's enchantment level. We now have an opcode that can get around that, but it needs to be applied.

That's what this mod is for.

This small patch grabs every magical missile launcher in the game (slings, crossbows, and the various bows) and applies an effect that
allows them to use their listed enchantment levels, regardless of what ammunition is being used with them.

That means if you have a +2 shortbow and normal arrows, it'll bypass creature defenses as if they were +2 arrows. (+3 arrows will still
function like +3 arrows; your equipped launcher can't make your equipped ammunition less magical than it is). This also means that an
end-game longbow doesn't also have to be paired with end-game ammunition in order to be usable against end-game monsters

It also means that infinite-ammo launchers like Firetooth and Gesen Bow are made more powerful by equipping real ammunition, not less.

Just install it like any other mod. It should work fine with BG:EE, SoD, and BGII:EE. Feedback is welcome!

## New Component: Ammunition Recovery
I spent a lot of time thinking about how best to handle ammunition. It doesn't make sense to me, for instance, that you can't recover
arrows that you use in combat--and picking up a dozen stacks of arrows obsessively because you don't want to go back to town seems like
a huge waste of time. That's the reason for increasing stack sizes in a number of tweak mods: to remove the headache of inventory
management so that you can focus on the parts of the game that are fun. Unfortunately, the inventory management is still there, it just
happens less often.

So. This thing.

The skinny: Any ammunition you purchase from a store is now treated as a rechargable quiver with a specific number of charges, which
recharges itself after every rest. This means that when you buy arrows, you're buying a quiver of 20 arrows; it will always be limited
to 20, but you'll start every day with a full quiver.

Each ammunition type has its own number of charges, as laid out below:
- Bolts: 20
- Bullets: 20
- Arrows: 20
- Throwing Daggers: 5
- Throwing Axes: 2
- Darts: 15

In addition, to keep things somewhat balanced, magical ammunition and thrown weapons have a maximum charge limit based on their particular
enchantment. A given weapon will use this limit or the base weapon's limit, whichever is lower:
- +1, +2, +3, +4: 10
- Minor Secondary Effect (such as Fire, Acid, Cold, or Electricity damage): 5
- Powerful Secondary Effect (such as Poison, Stunning, or Polymorph): 1

## Optional Components: Eldoth and Jan
Eldoth in BG:EE and Jan in BGII:EE have the ability to make their own ammunition as a 1/day ability, and the ammunition they create is pretty
powerful. No one wants to spend fifteen days stocking up on Poison Arrows, and when you forget to do it in the middle of a dungeon that can be
frustrating.

To that end, I've taken away from those characters the ability to create new ammunition, and instead given each of them a rechargeable version
of their special ammunition that has 5 charges.

That means you won't be able to stock up on Flasher Master Bruiser Mates, but it also means you'll always have five of them (and only five of
them) on hand, ready to go.

## Optional Component: Fix Fuller's Bolts
Fuller wants you to bring him some bolts. But because of the way the ammunition component above works, Bolts now cost 7 gp - and Fuller won't
take them from you. So this component just adds a single stack of bog-standard non-renewable bolts to the Candlekeep store, right at the top
of the list so you'll be able to spot them more easily.

## Notes
Pay attention to your characters if you use this component. There's a bit of a hitch where running out of charges on an ammunition item won't
prompt the character to switch to the next ammunition; they'll just stand there idly, waiting for death. You can fix it on the fly pretty easily
by switching ammo slots manually, but you'll want to pay attention to remember to do it.

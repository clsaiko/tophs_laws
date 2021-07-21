# Toph's Laws
This Crusader Kings 2 mod implements some additional laws for use by the player. I always found that in a late running game, I would run out of laws to have my council vote on. Eventually, laws were set to what I wanted them to be for the remainder of the game, so the council game became quite stale. By implementing additional laws which provide the liege with more tools with which to manage the realm, more fun might be had. To maintain balance, the laws should be balanced to not provide only benefit, but have drawbacks. I'm a fan of how the Roman Empire plays in game, so some of the laws are a little biased towards them.

## Imperial Usurpation - All Empires
Once Viceroyalties begin to be used, it becomes important that the liege creates and distributes any new titles to vassals as Viceroyalties. Vassals will make them nearly as soon as they are able, but unfortunately, there doesn't seem to be a way to change this behavior, as title creation conditions are hard coded for each title. There is no way to add a general requirement that could disallow vassals to make new titles, such as a liege having a law.

Most of the time, under a player emperor, kings will have the funds to create new duchies, and they will often create them as soon as they are able, such as after gaining land after winning a holy war. Sometimes, this occurs before the player is even notified they can create the new title. By granting an emperor the ability to usurp non-viceroyal duchies at will, this can help to remediate the problem. Though it comes at a cost, with -4 to all direct vassal opinion, and -8 to feudal vassal opinion, along with the standard opinion penalty from the character from whom a title has been usurped.

If the emperor so wishes, this may be extended to vassal republics and theocracies as well, though they come with an additional opinion penalty. There is a combination of gold, prestige, and piety cost to any of these.

## Imperial Senate - Roman and Byzantine Empires
The Imperial Senate, at least the later version of it created by Augustus, required Senators to be a substantial land owner and unpaid. They were more advisors and councillors to the Emperor, so in this implementation they must have a ducal title, be direct vassal of the Emperor, and will be granted a seat on the council. (Also unpaid.)

In exchange for a -10 vassal opinion hit, one council Consul title will be available to grant to those that meet the requirements, along with a bump in demesne limit (+1) and vassal limit (+5). The vassal limit is to account for the fact that there must be many more direct ducal vassals. In antiquity the Senate had some say in the appointment of a new Emperor, so they should be electors. Unfortunately, CK2 electors for a title are only the rank directly below it, in this case Kings, but Commanders are also electors. I don't really want to directly edit this aspect to allow Dukes, but since commanders are electors, I've modified the max emperor commander limit from 8 to 16, via the global define. This changes things for all other empires as well, but it makes no sense that large map painting empires should have just two more commanders than your basic King. (This number should really change for every ruler, as some function of realm size, but the commander_limit modifier seems to no longer work. The only option that appears to be left is to hardcode via this define, so here we are.)

After the Imperial Senate council law has been put into effect, Senate provinces must be enabled. To enable an Imperial Senate province the Emperor must hold the title. Once a province is enabled, the Kingdom will be destroyed, and that Kingdom will no longer be able to be created, by neither the Emperor, nor vassals, unless the Senate is dissolved. (Unlikely, once the Senate is established.) Each Imperial Senate province enabled will grant an additional +5 vassal limit. With each province brought under Senate control, an additional 2 Senate seats will be enabled (one for Sardinia/Corsica, one for Trebizond, three for Anatolia), to be appointed from the duchies that make up that Kingdom.

## Legates Augusti - Roman and Byzantine Empires
The Legates Augusti were literally envoys of the Emperor, governors which oversaw a specific province of the Roman Empire.

In exchange for a hefty -25 vassal opinion hit, a set of minor titles will be available to grant to those king vassals that meet the requirements, along with a bump in demesne limit (+2) and vassal limit (+5). Each title is opened with activating a province giving a further +5 vassal limit, and granting the minor title to a king that has a title in that province, as well as a seat on the council.

## Bestow Born in the Purple - Roman and Byzantine Empires
Add Born in the Purple trait to a grandchild. Technically, an unlanded child of the Emperor is living in the Imperial palace along with the Emperor. Aren't *their* children also Born in the Purple? Although there might be less of an aspect to this if the parent of the child is not yet risen to power, at least according to Wikipedia, but with this law, the Emperor may grant the Born in the Purple trait to a grandchild, by expending 600 gold and 600 prestige. In doing this, the Emperor spends extra resources and influence on their grandchild, introducing them and preparing them for potential rule. There are many requirements. The target must be a grandchild of the same dynasty to the current ruler of the Roman or Byzantine Empire, must be less than 1 year old, and must be a courtier of the Emperor. While strictly speaking this is no longer about location, but preparing for rulership, the Emperor's current capital must still be Constantinople or Rome. Stacking -5 feudal vassal opinion modifier for 20 years, for the Emperor's blatant disregard of tradition.

## Deactivate titular titles - All Kingdoms and Empires
Deactivate (and destroy) titular kingdoms. There are a few titular kingdoms here and there that, while they are neat to have and provide a bit of prestige, they end up being targets for factions, and only generate extra busywork for the ruler. Leaving them uncreated makes them able to be created by vassals, which when using viceroyalties is unacceptable. With this law, the player can remove the title completely for the remainder of the game playthrough. Cost of 1000 prestige.

## De Jure Edict - All Kingdoms and Empires
Transfer a Ducal title to be De Jure, under a King title. Sometimes, you just want a duchy to be under a king title faster, such as a merchant republic under your kingdom title as an emperor. By spending 1000 gold and 1000 prestige, the title may be put under a different Kingdom that is owned by the ruler. The ruler must only have one kingdom title. Stacking -10 feudal vassal opinion modifier for 10 years, for the ruler's sheer audacity.

## Additional Punishments - All Kingdoms and Empires
Additional punishment types for criminals and traitors. Normally, only Byzantine cultures may blind and castrate (gross). This law, when enabled, allows other cultures to use these as a punishment for crimes. As well, it introduces some additional punishments. Probation is just a temporary opinion modifier so the criminal is less likey to join factions, and partial blinding is simply a bit less severe than total blinding. Although there are other types that might be possible, they all seem to fall under these or existing punishments. Though this is not a crown law, the decisions are activated for all vassals if the top liege has the law. These give the ruler the ability to enact punishments that are less severe than what is in the standard game.

## Council Punishment Oversight - Dukes, Kingdoms, Empires
Some of the standard council powers available to implement is oversight of imprisonment, execution, and banishment. Some additional laws enable the council to vote on not just severe punishments like blinding and castration, but also the additional punishments implemented by the above laws. The council may act as a foil to the ruler, keeping him or her in check from being as much of a tyrant, but with the benefit of +2 to vassal limit for each law, if enacted.

These are separated into two groups:

Class I Punishments  - Probation, Humiliation, Torture

Class II Punishments - Any Blinding, Mutilation, Castration


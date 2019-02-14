# Enemies

## Introduction

Enemies are entites that are found within the world that may or not be hostile towards the player. In MMORPG games, enemies are usually the opportunity for the player's character to earn experience and earn items that drop.

Enemies have a few common aspects across the board. They often have a specific level and for that level can have a specific difficulty (for example, elite enemies in World of Warcraft). They also have some sort of scripting that enables the enemy to respond in a certain fashin towards the player. Each enemy does a specific amount of damage based on their level, difficulty and pool of abilities.

We'll first talk about leveling and scripting, and then propose alternatives to that specific implementation.

## Current Implentation for some games

### Level

In classical MMORPGs, enemies have their own level and their own difficulty for that level. For example, a monster at X level would be expected to be "simpler" to defeat than a boss at the same level.

### Scripting

Enemies are scripted driven, meaning that they can be expected to react to certain scenarios the same way. Often times, enemies have a specific rotation of abilities they use and their hidden abilities become apparent the lower HP they have. 

This is a very simplistic way to handle fights, and all that players need to do to win, is to simply memorize what enemies do at specific moments.

### Damage done

Enemies damage is often linked directly with their current level, their difficulty at that level and the pool of abilities they have at their disposal.

## New implementation proposal

### AI Difficulty Solution

With the removal of the leveling concept for playes, how should enemy diffculty be handled. Handled in a way, where the player would have a difficult time understanding how the enemy functions.

Using AI would bring a dynamic side to enemies removing the concept of memorizing and putting more empasis on player skill and reaction time.

Essentially, the idea would be to create various different AI's with a different complexity index.

Assume that we have the following, 7 different AI levels. (A direct reference to World of Warcraft Item Qualities)

1. Poor AI
2. Common AI
3. Uncommon AI
4. Rare AI
5. Epic AI
6. Legendary AI
7. God AI

(1) Poor AI would be a very simplistic unintelligent AI that would be applied to very unskilled enemies, where no resistance is expected. An example, would be to apply this to critters.

(2) Common AI would be a simplistic AI that would be applied to the majority of enemies. It allows the enemy to use a pool of abilities in a relatively smart manner. They are not "hard" to kill, but require some sort of attention. An average player should be able to handle 1-2 at a time.

(3) Uncommon AI would be a smart AI with good reaction time. They have a pool of abilities to choose from with a few hidden abilities. These monsters are the first generation able to analyze a player to find an advantage. An average player should find it difficult to kill one on their own. This AI could be attributed to enemies that belong to a respected race.

(4) Rare AI would be an intelligent AI with extremely good reaction time. They have a vast pool of abilities to choose from with many hidden abilities. They are able to analyze the group of enemies infront of them and to determine a winning strategy. They dont' hesitate to use the terrain to their advantage. This AI would be given to elit like enemies and smaller bosses.

(5) Epic AI would be an extremely intelligent AI with impossible reaction time. They have a vast pool of abilities to choose from with many hidden abilities. They will also have a pool of mass destructive abilities, that if not avoided would be instant kill. These enemies usually have a group of enemy followers to aid them and have strageically chosen the battlefield. This AI would be given to mini-bosses to bosses.

(6) Legendary AI would be extremely rare enemies that do not appear often. Their intelligence is to be recond with. In the fantasy world, they would be referred to as Dragons, Kings, etc. They are other worldy beings.

(7) God Like AI would be enemies on the level of Gods. They should be extremely exclusive and very difficult to come by and would require an enormous group of players to defeat.

### Why AI based ?

Nothing is as boring as perfectly remembering an enemy fight with all their phases and when everything can be expected.

There is a good meme out there that describes the situation that we seek.

> "Improvise. Adapt. Overcome."

This is something that should be rewarded rather than blatant memorization. When the world and the entities around keep suprizing players, that is truly memorable.

### Enemy Damage

AI controlled enemies does not determine how much damage that the enemy can do. The AI will simply determine the best outcome for that monster to win.

Each monster has its own features and abilities.

Lets take for example, a ferocious tiger (how scary). Its primary way of damage would logically come from its jaws and claws.

## Conclusion

[to be determiend]
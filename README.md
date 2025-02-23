# scoundel-cli

## How to play

Scoundrel is a single player dungeon crawler game that can be played with an ordinary deck of cards (or from the terminal).


### Monsters
Black suites are monsters. 
Monsters deal damage corresponding to their value (e.g. 2, 5, 10, etc)
J - 11
Q - 12
K - 13
A - 14

### Weapons

Diamonds are weapons.
Taking a weapon from the room discards any currently equipped weapon.
Using to fight a monster a weapon prevents damage from monster equal to the card value.
After fighting a monster with weapon can only use weapon to fight weaker monsters (e.g. after fighting a 9, can only fight 8 or below, after fighting a 2, can not use weapon any more).

### Recovering health

Player health starts at 20. 

Hearts are single use health potions.
Give health equal to number on card. Max 20 health.
Can only use one health potion per room.

### Beginning Play

Played with an ordinary deck of playing cards.
Remove all red face cards and red aces.
Remove jokers.
Shuffle remaining cards.

Deck placed face down.
Draw top four cards from deck (Enter Room)

### Turn

Pick a card from the room.
If its a weapon then equip that weapon, discarding any weapon currently equipped.
If its a health potion. Replenish health matching the value of the card, up to 20 health. Discard the potion.
If its a monster. Enter combat.

Repeat turn until only one card left in the room, then draw three more from the top.

### Combat

If weapon is not equiiped or weapon durability is too low:
  deduct health equal to monster card value
If weapon is equipped and durability not too low
  either:
    fight monster with barehands (take full damage)
    fight monster with weapon. 
      damage taken is difference between weapon value and monster value (e.g. weapon 5 and monster 8 applies 3 damage to player)
      weapon durability is set to monster value. Weapon can only be used to fight monsters of lower value than durability. (e.g. weapon value 8 used against monster value 9. Weapon durability is now 9, can only be used against monsters of value 8 or below)

### Running from a room

If at any point in time you cannot clear a room, you can choose to run from the room. 

Take all the cards in the room and place them face down on the bottom of the deck.

You cannot run from two rooms in a row.

### Ending the game

The game ends either when there are no more rooms left in the dungeon (win condition) or your health reaches zero.

---
title: Carnival tail
---
Carnival tail refers to the line of people and musicians following the player character around the town as they play the game. 

# Collision
When the player collides with the carnival tale one of the following happens: 
*(These are variants we want to explore before committing)*

## Game over
If the player collides with the carnival tail, the game ends and the player loses.

*Variation analysis:*
***Pros:*** 
*- easier to implement*
*- the game has an explicit lose condition*
***Cons:***
*- it's more frustrating experience*
*- might break player's flow state (mentally "getting into zone")*
## Tail cut off
If the player collides with the tail, the tail gets cut at the point of collision. Every person in the tail in behind of the collision (between point of collision and the carnival tail end) leaves the carnival a returns home. The buildings the people leaving the tail originate from will revert to the uncaptured, non-festive state and the player will need to recapture then in order to win the game. 

*Variation analysis:*
***Pros:*** 
*- less punishing for the player => less frustrating*
*- might help to cultivate player's flow state (mentally "getting into zone")* 
***Cons:***
*- requires tracking where people come from*
*- might have strange interaction with the way the people join the carnival tail (see [[Carnival tail#People joining in|People joining in]])*
*- game would not have an explicit lose condition*
# People joining in 
The people can join into the carnival one of the following ways: 
*(These are variants we want to explore before committing)*
## Waiting for the end
A new person joining joining the carnival tail will wait next to their building until the whole carnival tail passes by and then they join the carnival tail in the last position.  
![[carnival_tail_joining_wait_for_the_end.png]]

***Pros:*** 
*- this is how we generally expect well behaved people to join a line*
*- easy implementation*
*- good interaction with [[Carnival tail#Tail cut off|Tail cut off]]*
***Cons:***
*- after certain point, the player will not see the new people joining in (just them standing outside of the building)*
## Skipping the line
The whole carnival tail excluding the player character will stop for a moment to create space for the new person joining. The new person then joins the carnival tail in the position right behind the player character.
![[carnival_tail_joining_skip_ahead.png]]
***Pros:*** 
*- player will get to enjoy the art of new people for a bit*
*- still a good interaction with [[Carnival tail#Tail cut off|Tail cut off]]*
***Cons:***
*- people might seem a bit rude*
*- harder to implement*
*- player will not get to see the older art for long*
*- there will be a lot of movement on the screen*
*- might break the feel of the line following the player*

## Joining at random position
The whole carnival tail excluding the player character will stop for a moment **after walking for a random amount of time** to create space for the new person joining. The if the amount of time The new person then joins the carnival tail in the position right behind the player character.
![[carnival_tail_joining_join_at_random_possition.png]]
***Pros:*** 
*- player will get to enjoy the art of some new people joining while not losing the old art*
*- the line will seem more organic and less structured, adding to the spontaneous mood*
*- kind of natural way of people joining in*
***Cons:***
*- the hardest to implement*
*- strange interaction with [[Carnival tail#Tail cut off|Tail cut off]]*
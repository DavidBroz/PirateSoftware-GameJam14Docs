---
title: Movement
---
# Graph based pathing
The player character walks around the streets of the town on like on a graph. Each pavement is an edge and every crossing is a node. When player character arrives to an edge. 

Following are considered to be edges of the graph:
- Pavements 
- Crosswalks
![[game_world_as_graph.png]]
# Auto walking
The player character is moving automatically in their current direction without stopping at set speed. In the sense of the graph view that means the player character can change their movement direction **only on nodes**.

# Change of direction
When the player character walks into a pavement crossing (a node in the graph view) they can change a direction of their walk. 

***Player character cannot turn around.*** On a pavement crossing (a node in the graph view) the player character cannot walk along the pavement (edge) they arrived there on. 

![[movement_changing_directions.png]]
## Controls 
The movement not the pavement (edges of the graph) can be controlled by the player using the **keyboard keys**
![[Keybindings#Movement keybidings]]
### Input buffer
The players input can be buffered so if the player presses the key before the player character reaches a crossing of pavements (node) the input is stored and used when the character reaches the correct point. 

The duration of the buffered input is adjustable with [[Movement#Parameters|parameters]] 
## Default direction order
If player character walks into a pavement crossing (node) without any buffered player input, the characters will chose direction according to following priorities:
1. Keep the current direction
2. Turn right
3. Turn left
The player character without buffered input will try to go in the highest priority direction first and only if they are unable they move to the next.
# Parameters
![[Game parameters#Movement]]

---
title: Movement
---
# Graph based pathing
The player character walks around the streets of the town on like on a graph. Each pavement is an edge and every crossing is a node. When player character arrives to an edge. 

![[game_world_as_graph.png]]
# Auto walking
The player character is moving automatically in it's current direction without stopping. In the sense of the graph view that means the player character can change their movement direction **only on nodes**.

# Change of direction
When the player character walks into a pavement crossing (a node in the graph view) they can change a direction of their walk. 

***Player character cannot turn around.*** On a pavement crossing (a node in the graph view) the player character cannot walk along the pavement (edge) they arrived there on. 

![[movement_changing_directions.png]]
## Parameters
A parameters that can be set by the `game_parameters.ini` file 
- `walking_speed` = player character speed over an edge
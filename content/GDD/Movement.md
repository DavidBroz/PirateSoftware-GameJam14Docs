---
title: Movement
---
# Graph based pathing
The player character walks around the streets of the town on like on a graph. Each pavement is an edge and every crossing is a node. When player character arrives to an edge. 

![[game_world_as_graph.png]]
# Auto walking
The player character is moving automatically in their current direction without stopping at set speed. In the sense of the graph view that means the player character can change their movement direction **only on nodes**.

# Change of direction
When the player character walks into a pavement crossing (a node in the graph view) they can change a direction of their walk. 

***Player character cannot turn around.*** On a pavement crossing (a node in the graph view) the player character cannot walk along the pavement (edge) they arrived there on. 

![[movement_changing_directions.png]]
## Default direction order
If player character walks into a pavement crossing (node) without any buffered player input, the characters will chose direction according to following priorities:
1. Move forward
2. Move right
3. Move left
The player character without buffered input will try to go in the highest priority direction first and only if they are unable they move to the next.
# Parameters
A parameters that can be set by the `game_parameters.ini` file 
- `walking_speed` = player character speed over an edge
- `input_buffer_time_ms` = for how many milliseconds is player input buffered for 
# Concept: 'Ant Trail'

## Team Members
- Marie-Lena Müller 
- Daniel Rajs 
- Richard Schultheis 
- Eric Eckstein

## Targets
We want to create an ant trail application in unreal engine.  
The goal is to have a colony of ants placed in the middle of a map. The ants do need to provide
food for their colony. Therefore all ants will leave the colony looking for food in random directions. If they do not find food in a defined time they will return to the colony. Once an ant finds a food source they will pick up a part and carry the food back to the colony.  
The ant will leave an information trail while returning to the colony, so other ants can follow that trail to find the food source.

## Algorithms
The ants need to find a way in probably blocked terrain. So we will implement an wayfinding algortihms, like A*.  
The ant agent will be probably controlled by a finite state machine
see: [Paper: Solving Five Instances of the Artificial Ant Problem with Ant Colony Optimization](https://www.sciencedirect.com/science/article/pii/S1474667016344275) and [Unreal Wiki on Finite State Machines](https://unrealcommunity.wiki/revisions/616a17485229ed20458b1471)

# Timetable / Effort

## Map Setup
First we want to create a static map that contains 2-3 food sources, blocking terrain and the colony. Later this might be generated in a random way. This will be mostly modeling without materials or animations.  
**Estimation: 20h**

## AI control
Second we want to implement the "AI", probably finite state machines controlling the ants.  
**Estimation: 30h**

## Materials:
We need materials for
- the ant
- grass
- blocking terrain like stones or trees or branches
- food on the ground, like apples or dead wasps
This will be used to create blueprints that look good and will be reused.

**Estimation: 20h**

## Lighting:
We want to have a real sun like lighting. So we want a static sun like lighting from a higher corner throwing shadows on the map. In a later stage we might use a daylight circle where we have day and night phases changing the light. This might also be user controlled in the UI.  
**Estimation: 10h**

## Particles:
We want to create the pheromone trail ants leave behind as particles to make them visible.  
**Estimation: 25h**

## Audio:
Some windy forrest sounds in the background. There will be sound effect when a ant finds a new food source or when a ant finds a pheromone trail of another ant.  
**Estimation: 20h**

## Animations
We will animate the movement of the ant agents. Also there should be a animation for an agent picks up food and the delivery back to the colony (which is different to the default walking animation)  
**Estimation: 40h**

## Player HUD + Menu
We do not want the player to have an active part in the simulation. Though the player should be able to move the camera through the map. Also the player should be able to start, stop and continue the simulation. Also will be a way to reset the simulation to start. (Probably when we can randomly create maps)  
**Estimation: 25h**

## Meetings & project setup
Github repo setup, meetings, overhead  
**Estimation: 20h**


# Milestones

| Task                          | Done by               | Effort    |
| -------------                 |:-------------:        | -----:    |
| Map Setup                     | 18.04.2022            |   20h     |
| AI Control                    | 02.05.2022            |   30h     |
| Player HUD                    | 02.05.2022            |   25h     |
| Materials                     | 02.05.2022            |   20h     |
| Lighting                      | 15.05.2022            |   10h     |
| Particles                     | 27.05.2022            |   25h     |
| Audio                         | 27.05.2022            |   20h     |
| Animations                    | 27.05.2022            |   40h     |
| -----------------             | --------------        |   ----    |
| Implementation                |                       |   190h    |
| Meeting & project setup:      |                       |    20h    |
| -----------------             | --------------        |   ----    |
| Overall:                      |                       |   210h    |


# Blueprint Learning Notes

## Introduction to Blueprints

- Blueprints are visual scripting in UE5.
- They allow designers to create gameplay elements without coding.

## Blueprint Components

1. **Event Graph:**
   - Main graph for handling events.
   - Write custom logic using nodes.

2. **Construction Script:**
   - Used for construction-related logic.

## Tips for Efficient Blueprinting

- Keep graphs organized.
- Use comments to explain complex logic.
- Reuse functions for modularity.

![Blueprint Example](images/blueprint_example.png)


## Tips
**Actor:** 
An Actor is a fundamental building block in UE5. It is a container for Components, and it can be placed in the game world. Actors can be anything from characters and props to lights and cameras.

**Pawn:**
Pawns are Actors that can be possessed by players or AI controllers. They represent entities that can be moved around in the game world. Characters are a common example of Pawns.

**Player Controller:**
This class manages input from players and communicates with Pawns. It helps in controlling the player's viewpoint and interaction with the game.

**Character:**
A Character is a type of Pawn that includes additional features like a mesh, a skeletal mesh, and built-in movement components. It's often used for representing playable characters in the game.

**Game Mode Base:**
This class defines the rules of the game, such as which Pawns and Controllers to use, the win/lose conditions, and other game-specific logic.

**Actor Component:**
Components are modular parts that can be added to Actors to give them specific functionality. Actor Components are reusable pieces of functionality that can be attached to different types of Actors.

**Scene Component:**
Scene Components are components that define a transform in the game world. They are often used for positioning and transforming other components attached to them.

Choosing the right class depends on the functionality you want for your game object. If you're creating a player character, you might choose the Character class. If you're creating an inanimate object, like a lamp, you might choose the Actor class. Components are then used to add specific features, like movement, collision, or visual appearance.

**Constant Material Expressions:** 
   - Material Expressions whose outputs generally do not change once set in the Editor or when play begins. 
   - **Shortcut key:** press and hold 1 and left mouse button.
   - or type just type constant with left mouse button.
   - We can use this not to build materials 
  - Example : 
    - glass material: 4 constant nodes we gone need here to set value between 0 and 1. And to achieve all the require parts of materials we need do settings as follow. In side the Material section setup **Blend Mode to Translucent** and In side of Translucency section setup **Lighting mode to Surface TranslucencyVolume**. and then setup the value of all 4 constant nodes as follow.
    1. Base color Node with the value = 1.0
    2. Metallic Node with the value = 1.0
    3. Roughness Node with the value = 0.06
    4. Opacity Node with the value = 0.2


**Event Begin Play:** (Node)
   - The "Event Begin Play" node is triggered when an instance of the Blueprint is spawned or the level containing the Blueprint is loaded. This event is particularly useful for setting up initial configurations or executing actions that should happen only once when the game or level starts.

   - For example, if you want to initialize variables, spawn additional actors, or trigger a specific sequence of events at the beginning of the game or level, you would use the "Event Begin Play" node.

   - You can find this node by right-clicking in the Blueprint graph, searching for "Event Begin Play," and then connecting your desired nodes to its execution pin.

**Event Tick:** (Node)
   - The "Event Tick" node is continuously executed every frame during gameplay. This event is handy for implementing logic that needs to run continuously, such as updating the position of an object, checking for player input, or managing dynamic game states.

   - It's important to use the "Event Tick" node judiciously because its frequent execution can impact performance. For tasks that don't require constant updates, using other events or triggers may be more efficient.

   - To use the "Event Tick" node, you can find it in the Blueprint graph by right-clicking and searching for "Event Tick." Connect the desired nodes to its execution pin for continuous execution.

Here's a simple example to illustrate the usage:

- **Event Begin Play:** Set up initial configurations, spawn actors, or perform actions that need to happen once at the start of the game.

- **Event Tick:** Continuously update the position of a moving object, check for player input, or manage dynamic states during gameplay.

Always be mindful of performance considerations, especially with the "Event Tick" node, as executing too many operations every frame can impact your game's frame rate. If you have specific scenarios or functionalities in mind, feel free to provide more details, and I can guide you through their implementation!




## Important Nodes:
**Red color nodes : *Event nodes*** - red-colored nodes in the Blueprint editor typically represent Event nodes. These nodes are essential for handling various game events. Here's a detailed list of common red-colored Event nodes along with their functionalities:

1. **Event Begin Play:**
   - **Functionality:** Executes when the game starts or when the Blueprint is first spawned.
   - **Use Case:** Initialize variables, set up initial game state, or perform other actions needed at the beginning.

2. **Event Tick:**
   - **Functionality:** Executes every frame during gameplay.
   - **Use Case:** Continuously update and check conditions during gameplay.

3. **Event Actor Begin Overlap:**
   - **Functionality:** Triggers when the Blueprint's actor overlaps with another actor.
   - **Use Case:** Implement logic for interactions when two actors come into contact.

4. **Event Actor End Overlap:**
   - **Functionality:** Triggers when the overlap between two actors ends.
   - **Use Case:** Implement logic for actions to be taken when two actors are no longer in contact.

5. **Event Hit:**
   - **Functionality:** Activates when the actor is hit by a physical collision.
   - **Use Case:** Implement responses to collisions, such as damage calculations or visual effects.

6. **Event Destroyed:**
   - **Functionality:** Executes when the actor is destroyed.
   - **Use Case:** Clean up resources or perform actions before the actor is removed from the game.

7. **Event Any Damage:**
   - **Functionality:** Triggers when the actor receives any form of damage.
   - **Use Case:** Implement custom logic for handling damage events.

8. **Event Actor OnClicked:**
   - **Functionality:** Activates when the actor is clicked in the game.
   - **Use Case:** Implement actions based on player interaction, like opening menus or triggering events.

9. **Event Actor OnReleased:**
   - **Functionality:** Triggers when the mouse button is released after clicking on the actor.
   - **Use Case:** Implement actions based on the release of the mouse button.

10. **Event Timer:**
    - **Functionality:** Executes when a specified timer expires.
    - **Use Case:** Implement timed events or actions in the game.

These are some of the fundamental red-colored Event nodes in UE5 Blueprints. Each serves a specific purpose in controlling the flow and behavior of your game.
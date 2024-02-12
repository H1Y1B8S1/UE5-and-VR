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
 
 **Constant:** 
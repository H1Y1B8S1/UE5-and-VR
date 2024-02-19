# Performance and FPS settings
**Increase fps when so many nanite obj like tree in level**
- IN Rendering (setup this values) 
  - Shadow Map Method = Shadow Maps
  - Anti-Aliasing method = TAA


# Problem solutions

**Shadow problem:**

1. directional Light - Cast Ray traced Shadows = toggle it to Disable or Project setting instead Enable.
2. or keep Enable Cast Ray traced shadows and set value 0 to the r.RayTracing.Shadows.EnableTwoSidedGeometry in cmd. By default it is 1.
   *r.RayTracing.Shadows.EnableTwoSidedGeometry 0*
   - here we have a problem where after setting value to 0 1 sided objects wont produce shadows.
3. error value change apply on nanite mesh to 0 (Not recommended).







# OPEN WORD MAP SET UP

**Light setup:**

- Directional light - make it movable.(if we want more sun change or increase **atmosphere sunlight index** )
   - Change the color of sun by changing value of **Temperature** in Details.
- Sky light - make it movable and check **Real time capture**.
- Exponential height fog - 
- Volumetric Cloud - 


**build LandScape Material:**
- Enable fully rough for the material.
- add node called **landscape Layer Blend**.
   - Add layers in array, and give names **without space in name**.
   - Blend type = LB Weight Blend.
- now bring Materials Base Color (2nd one) to event graph and connect RGB to each layer blend. And connect Layer blend to **Base color**.
- Now same process with **Normal map (3rd one)**. duplicate the Layer blend and connect all the normal maps. And connect Layer blend to **Normal**.
- Now add this material in whichever landscape we want to paint.
- Now go in LandScape mode and choose paint, then at bottom create material info my click **+** on each material and save in folder.
  
**Plant painting: straight to land**
- Go to foliage - placement- uncheck align to normal to grow straight instead side way on heels.

**Adding Collision in multiple OBJ: Bulk edit via Property matrix**
- Select all the obj we want to add collision in then select right click.
- **Asset Action - Bulk edit via Property matrix**
- Set value **BlockAll**(by typing) in Collision profile name.

**PostProcessVolume:**
- Add postprocessvolume from the place Actor tab
- check **infinite Extent (unbound)**










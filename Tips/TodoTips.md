**Shadow problem:**

1. directional Light - Cast Ray traced Shadows = toggle it to Disable or Project setting instead Enable.
2. or keep Enable Cast Ray traced shadows and set value 0 to the r.RayTracing.Shadows.EnableTwoSidedGeometry in cmd. By default it is 1.
   *r.RayTracing.Shadows.EnableTwoSidedGeometry 0*
   - here we have a problem where after setting value to 0 1 sided objects wont produce shadows.
3. error value change apply on nanite mesh to 0 (Not recommended).
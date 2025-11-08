# Light Generator

![light-thumb](https://github.com/user-attachments/assets/b68dc89e-2af7-4b1e-b0fa-7336c361f63b)

**Author:** The French Monkey (TFMSTYLE)  
**Version:** 1.2.3  

---

## Overview

The Light Generator creates multiple light sources distributed across 3D space using procedural patterns and customizable layouts.  
It provides control over light count, distance, spacing, intensity, and randomization — all organized under a parent generator object.  
Lights can be distributed in patterns such as rings, grids, spheres, domes, or spirals, and can also be saved as reusable **presets**.  
The system is ideal for product visualization, lighting studies, environment setups, or stylized renders requiring complex multi-light arrangements.

---

## Parameters

### Light Count
Defines the number of light objects to generate and manage within the active light generator.

---

### Distance From Target
Specifies how far the lights are placed from the target point or object.  
Affects the overall radius or spread of the light layout.

---

### Distance Randomizer
Applies random variation to each light’s distance from the target to avoid perfect symmetry.

---

### Z Offset
Adds a vertical offset to all generated lights.  
Useful for lifting or lowering the light formation above or below the target.

---

## Light Type & Shape

### Light Type
Defines the kind of light to generate:
- **Point:** Emits light in all directions from a single point.  
- **Area:** Emits light from a flat surface with adjustable shape and size.  
- **Spot:** Emits a cone-shaped light beam, ideal for focused illumination.

---

### Area Shape
When using Area lights, selects the emission shape:
- **Square** — Equal dimensions in X and Y.  
- **Disk** — Circular light source.  
- **Rectangle** — Rectangular light with independent X and Y sizing.

---

### Size
Controls the overall size of the Area or Disk light surface.

---

### Size X / Size Y
When using **Rectangle** area lights, defines individual width (X) and height (Y) dimensions.

---

### Radius
For Point and Spot lights, defines the light’s softness radius (affecting shadow softness and light spread).

---

## Light Power

### Randomize Light Power
Enables random energy variation between lights to create a natural or uneven lighting setup.

---

### Min Power
Minimum possible light intensity when randomization is enabled.

---

### Max Power
Maximum possible light intensity when randomization is enabled.

---

### Seed
Controls the randomization pattern for power distribution.  
Changing this generates a new random variation.

---

## Spacing Method

### Spacing Method
Defines how lights are spatially distributed around the target point or object.  
Available options:

- **Random:** Lights are placed randomly in 3D space within the specified distance.  
- **Ring:** Evenly distributes lights in a circular ring around the target.  
- **Sphere Grid:** Evenly spaces lights across a spherical grid layout.  
- **Spiral:** Generates lights along a spiral path extending outward.  
- **Grid:** Organizes lights into a 2D rectangular grid pattern.  
- **Line:** Positions lights in a straight linear formation.  
- **Dome:** Generates lights in a hemispherical dome above the target.  
- **Preset:** Loads and applies a custom light setup from a saved preset.

---

### Grid Line Point Down
For Grid and Line spacing modes, toggles between lights pointing toward the target or pointing directly downward.

---

### Random Seed
Controls the random placement pattern for all spacing modes that use randomness.

---

## Targeting

### Use Target Object
When enabled, lights will orient themselves to aim at the selected target object instead of the world origin.

---

### Target Object
Specifies the object the lights should aim toward.  
When unset, lights target the global origin (0,0,0).

---

## Spot Light Settings

### Spot Size
Defines the cone angle (in degrees) of Spot lights.  
Higher values result in wider light beams.

---

### Spot Blend
Controls the smoothness of the light’s falloff near the edge of the cone.  
Higher values create a softer transition.

---

## Presets

### Selected Preset
Stores the name of the currently selected lighting preset for reapplication or deletion.

---

### Preset Storage
Presets are saved as JSON files inside the add-on’s data folder.  
Each preset records all light positions, rotations, colors, intensities, and types.

---

## Additional Options

### Select All Lights
When enabled, all generated lights under the active Light Generator are automatically selected in the viewport after creation.

---

## Operators

### Generate Lights
Creates a new Light Generator or updates the selected one with the current parameters.  
Automatically populates it with the configured light distribution.

---

### Delete Lights
Removes the selected Light Generator and all its associated light objects.

---

### Save Current Lights as Preset
Saves the current Light Generator’s configuration and all child lights as a reusable preset.  
Prompts for a preset name before saving.

---

### Delete Selected Preset
Removes the currently selected preset from the preset file.

---

### Preset Menu
Lists all available presets.  
Selecting a preset automatically applies its stored lighting configuration.

---

## Usage Notes

- Begin by adjusting **Light Count** and **Spacing Method** to define the overall layout.  
- Use **Distance From Target** and **Z Offset** to refine the formation’s size and height.  
- Choose **Light Type** and **Area Shape** to control how each light behaves.  
- Enable **Randomize Light Power** to introduce variation and realism.  
- Use **Use Target Object** to focus all lights on a specific model or scene element.  
- Save frequently used configurations as **Presets** for rapid scene setup.  
- The generated Light Generator is a parent object — moving or rotating it moves all lights together.  
- Each light remains a fully editable Blender object with standard lighting properties and materials.

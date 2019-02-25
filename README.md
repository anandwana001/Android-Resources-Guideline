# Android-Resources-Guideline

This repository consist the best practice of Android Resources
We will be going through each one
- anim
- animator
- color
- drawable
- layout
- menu
- raw
- mipmap
- xml
- font
- values
  - styles
  - colors
  - dimens
  - attrs
  - strings

## Styles
 - Do not create style for a single use
 - Do not create style for group attributes like padding, margin etc
 - Naming convention of a style: 
    - follow the parent name
    - parent=”@style/Widget.AppCompat.Button”
    - name=”Widget.MindOrks.Button” 
  - Do not use layout_* attributes in style file. This is for layout files and also not duplicate even if the require same
  - Use of dimesnions for duplicate layout_* file should be done very carefully
  - Do not hardcode the value of parameters in style
  - Specify one style and redirect to other resoucre variable that point to different resources based on each configuration
  - Try to use appCompat resources as much as we can rather than going to create own style
  - All style should have parent to get default property of widget
  - We can have multiple style files like styles.xml, styles_homepage.xml, styles_item_details.xml
 
## Colors
  - Use RGBA value for defining color
  - Always put a small comment above the color to make it more understandable
  
 ``` 
 <resources>
    <!-- grayscale -->
    <color name="button_primary">#FFFFFF</color>
   
    <!-- basic colors -->
    <color name="button_secondary">#2A91BD</color>
</resources>
```
  
  - Color naming convention
    - name by it's function
    - avoid naming by colors like bkue, green etc
    - We can give name on the basis of transpreny like black_60pc for #80000000
    - We can also use general terms like dark, super_dark, light 
  - Define color palettes
  
  ```
  <!-- Palette colors -->
    <!-- Colors for "general use" only -->
 
    <!-- General palettes -->
    <color name="black_solid">#000000</color>
    <color name="you_tube_red">#A20015</color> 
    <color name="bondi_blue">#00A8B0</color>
    <color name="white_solid">#ffffff</color>
    
    <!-- Gray Palettes -->
  ```
  ## Drawable
  - Naming convention of drawable files
    - `<type>_<group>_<subgroup>(_<variant>).xml` example - bg_button_primary.xml
    - common prefix ic for icon, bg for background and div for dividers

  ## Layout
  - Common prefix for layout file names
    - activity_
    - fragment_
    - view_
    - item_

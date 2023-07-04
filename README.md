# maperitive_rules
Repo containing maperitive mrules files for displaying OpenStreetmaps data differently for various applications

# Requirements
* Working installation of maperitive (Free Software from maperitive.net)

# Adding New Rules
1. Determine what rules file you want to have available
1. Determine the alias it'll appear in the maperitive menu as
1. Determine where you want the alias to appear in the list of rules (Default is last in the list)
1. Copy the .mrules file you want from this repo into the 'rules' folder within your maperitive installation (Windows default would be 'C:\Program Files\Maperitive\Rules')
1. Start Maperitive
1. In the "Command Prompt" box at the bottom enter `use-ruleset location=rules\<RULEFILENAME>.mrules as-alias="<Rule Alias Name>" index=<index number>`
  1. `<RULEFILENAME>.mrules` should be replaced with the actual filename of the rule file
  1. `<Rule Alias Name>` should be replaced with the alias you want to appear in the rules list in Maperitive
  1. `<index number>` is optional and should be replaced with an integer indicating where you want the alias to appear in the rule list

# Rules
## Laser.mrules
* Only display roads, water, railroads, trails, etc
* No parks, buildings, etc
* include road names

## LaserNoTrails.mrules
* same as Laser but do not include trails

## LightBurnLayers.afpalette
Affinity Palette file (Designer and Photo) that maps to layers in Lightburn upon import.  To import the pallette into Affinity Designer or Photo:
1. Open Affinity Designer
1. Ensure the "Swatches" window is enabled<br>
    ![Enable Affinity Swatches](/media/affinity_swatches.png?raw=true "Enable Swatches window in Affinity Designer")
1. With swatches enabled, access the swatches panel.  NOTE: Your display could be configured completely differently than mine, finding the swatches panel is beyond the scope of this document.<br>
    ![Access Swatches](/media/affinity_find_swatches.png?raw=true "Access Swatches panel")
1. In the swatches panel, drop down the 'hamburger menu' in the top right and select "Import Palette", then "As Application Palette".<br>
    ![Import Palette](/media/affinity_import_palette.png?raw=true "Import Palette in Affinity Designer")
1. In the Swatches Panel, use the Palette dropdown to access the newly imported palette<br>
    ![New Palette](/media/affinity_new_palette.png?raw=true "New Palette in Affinity Designer")
1. Using colors from this palette in Affinity will import objects into Lightburn in the corresponding layers!

NOTE: The last two colors in the palette match the "tool layers" in Lightburn.  These colors are not honored during import in the current versions of Lightburn and therefore, anything using these colors in Affinity will be mapped to the "Nearest valid color" layer in Lightburn.

## Changelog
* Dropped LaserNoText.mrules, text is always on a different layer so easily removed in Affinity/Illustrator/Inkscape
* Improved River/Stream handling to provide shape outlines of Rivers and Streams instead of just the main line
* Added Affinity Palette file for Lightburn Layers

## Reference
[Lightburn Layer Color Codes](LightBurn_Layer_colors.md) for importing SVG into Lightburn later
[Video](https://youtu.be/5GSa7g4568M) of using the rules in this repo

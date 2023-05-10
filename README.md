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
* Only display roads, water, railroads, etc
* No parks, buildings, etc
* include road names

## LaserNoText.mrules
* same as Laser but do not include names

## Changelog

## Reference
[Lightburn Layer Color Codes](LightBurn_Layer_colors.md) for importing SVG into Lightburn later

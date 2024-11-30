# Vehicle Editor Absurdifier
The Absurdifier is an extensively modified clone of the global Vehicle Editor template.

## Installation
This mod requires a two-step process:

### Package Installation
Use the [Spore ModAPI Launcher Kit](https://davoonline.com/sporemodder/rob55rod/ModAPI/Public/)'s _Easy Installer_ app or the [Spore Mod Loader](https://github.com/Rosalie241/SporeModLoader) command-line to install the `.package`. 

### State Configuration
Due to being an independent Editor, a custom game state is required. This neccesitates a modified App States list (`SporeAppStates.txt`) including this new state. The file provided along with the mod in the Releases page. Save this new list to your `..\(Spore) Galactic Adventures\DataEP1\Config` folder. Most distribution platforms will likely have an option in the Properties menu for the game that takes the user directly to the game's installation directory. This will now allow the Editor to be accessed through Command Line or through a modified shortcut to the game, appending `-state:AbsurdVehicleEditor`. Most platforms will have an option in the Properties menu for the game to allow users to specify Command Line options.

**Note:** The Absurd Editor cannot be re-entered this way until the game is restarted, unless using the **EnterEditor** mod listed under _Suggested Mods_. Future versions _might_ include a way to do so.

## New Mechanics
Technically not "new", but the mod features mechanics ported over from the Building Editor:
* Hold `Ctrl` while moving a part to move it on its Z (Up/Down) Axis.
* Hold `Shift` while moving a part to move it on its XY (Front/Back + Left/Right) Plane.
* Save as any Vehicle / Building by adjusting selecting an option from the list in the lower left. This excludes UFOs due to being programmed differently than other type of Vehicles. See _Suggested Mods_ for more details.

**Note:** due to such mechanics being unintended for Vehicles, shifting certain parts (i.e. Chassis and Cockpits) off of their axis of symmetry can have unexpected behaviours. See _Suggested Mods_ below for more details.

_Technical note: the mod also features the Creature Editor-specific capability to manipulate limbs (specifically limited to 'solid' limbs (i.e. the Exoskeletal ones, and several added by Dark Injection, including Invisible ones)). No known released mod adds limbs like these to the Vehicle or Building Editors, but if one does appear, this Editor can implement them without further modification._

## Increased Limits
The boundaries of this Editor are considerably larger than any other version of the Editor, to frankly _absurd_ degree:
* Height Limit: Upwards and Downwards height limit increased by 25x (from 10 in either direction to 250 in either (or from 20 in total to 500 in total)).
* Radial Limit: Radius limit of the editor increased by roughly ~42x (from 6 units in radius to 250 (or from 12 in diametre to 500)).
* Part Limit: Part limit increased to 1023 total parts (crashes if saved at 1024 excatly, and passed 1024 fails to load correctly after restarting the game).
* Budget and Complexity: The part budget and complexity budget have both been increased to 999,999, effectively eliminating any concern for part costs outside of modded parts with purposefully high costs.

## Handle Modifications
Due to the way Spore's Editors are programmed, Morph Handles, Rotation Rings, Rotation Balls, etc. are scaled proportional to the given Editor's boundary size. This present an issue, as while an Editor can be configured to use custom handles, the convoluted manner in which Rotation Rings are handled means that they cannot properly be configured specifically for this Editor, meaning that changes have to be applied globally. This has the unfortunate side effect of making Rotation Rings univerally smaller to accomodate hte Absurd Editor's increased boundaries, rendering them effectively useless in other editors so long as this mod is installed.

This may be fixed later, but may require scripting, in turn requiring the use of the Spore ModAPI Launcher Kit or Spore Mod Loader.

## Suggested Mods:
These mods are compatible with and expand on the Absurd Vehicle Editor, though not all add content to the AVE directly. Mods requiring the SMAPILK or SML are indicated with an `&`:
* (&) [EnterEditor](https://github.com/VanillaCold/SporeEnterEditor) by VanillaCold : Allows the user to access the Editor via the Cheat Console instead of being limited to only being able to run it from Command Line or Shortcuts. It can also be used to open Absurd Vehicles in any other Editor, including the UFO Editor. Doing this allows the user to access parts not directly available in the AVE, but in normal versions of the Vehicle Editor. The ID of the AVE is `vehicleabsurd`, therefor the command would be `entereditor vehicleabsurd` or `editcreation vehicleabsurd`.
* [The Means of Production](https://mega.nz/file/TMF3TLjC#-6n4fzY6hbNE-oO_jRFEl0du5D8IGEVfe6Kaqnnx0yI) by vainglory : Adds every category of part to every Vehicle Editor - including the UFO Editor. Additionally, adds non-animating and effect-less duplicates of every relevant part.
* [BioTech Parts](https://www.mediafire.com/file/n47frrzn5ppfo9h/BioTech_Parts.package/file) by mx3brainpower and Lord Tenebris : Adds most Creature Editor Parts to the Vehicle Editors, including animations. Abandoned project, some parts have not been completely ported in a polished state. **Warning: beware ads on MediaFire pages**.
* [Port and Starboard](https://github.com/Valla-Chan/Spore-Mods/releases/tag/SporePortAndStarbord) by Valla-Chan : Adds duplicates of the Vehicle Editor cockpits and chassis that function as detail parts, allowing you to place them on the sides of vehicles. Useful for sidestepping issues with Building Editor mechanics being used on those parts.
* (&) [Wordsmith](https://github.com/Valla-Chan/Spore-Mods/releases/tag/SporeMod) by Valla-Chan : Adds letters from the Latin, Hiragana, and Katakana alphabets, as well as numbers and a few symbols, into the Vehicle (and Building) editors.
* [Building & Vehicle Fusion](https://davoonline.com/phpBB3/viewtopic.php?f=118&t=5021) by mx3brainpower : Adds all vanilla Vehicle Parts into the Building Editor's palette and vice-versa.
  * [Building-Vehicle Fusion Snapping Fix](https://github.com/Valla-Chan/Spore-Mods/releases/tag/Spore_BVfusion_SnapFix) by Valla-Chan : An addon for the above mod which fixes the vehicle parts to properly stack and align to the center of other parts when used in the Building Editor.
* (&) [Cheatbox](https://github.com/MADPSI/Cheatbox) by MADPSI : An extensive collection of cheats and keybinds that expands the functions of the Editors. Includes a cheat and bind for panning the camera and creating a placement grid, both available in the AVE.

## Acknowledgements
* [Splitwirez](https://github.com/Splitwirez) : Early developement assistance.
* [ACyborgSquid](https://www.spore.com/view/myspore/MythicalMist) (MythicalMist) : _Extensive_ beta testing, troubleshooting and "free publicity".
* All above mentioned suggested mod makers.
* [DarkEdgeTV](https://x.com/DarkEdgeTV) : _Indirect_ suggestions.
* [VanillaCold](https://github.com/VanillaCold) : AVE inspired by [Advanced CE](https://github.com/VanillaCold/Spore-AdvancedCE) mod.

# Vehicle Editor Absurdifier
The Absurdifier is an extensively modified clone of the global Vehicle Editor template, that is to say the master from which all other kinds of Vehicle Editor are derived. Instead of being a modification of any of those, it exists as its own seperate entity.

## Installation
This mod has a slightly more complicated than usual two-step process:

### Package Installation
Use the [Spore ModAPI Launcher Kit](https://davoonline.com/sporemodder/rob55rod/ModAPI/Public/)'s _Easy Installer_ app or the [Spore Mod Loader](https://github.com/Rosalie241/SporeModLoader) command-line to install the `.package`.

### State Configuration
Due to being an independent Editor, a custom game state is required. This neccesitates a modified App States list (`SporeAppStates.txt`) including this new state. The file provided along with the mod in the Releases page. Save this new list to your `..\(Spore) Galactic Adventures\DataEP1\Config` folder. Most distribution platforms will likely have an option in the Properties menu for the game that takes the user directly to the game's installation directory. This will now allow the Editor to be accessed through Command Line or through a modified shortcut to the game, appending `-state:AbsurdVehicleEditor`. Most platforms will have an option in the Properties menu for the game to allow users to specify Command Line options.

**Note:** The Absurd Editor cannot be re-entered this way until the game is restarted, unless using the **EnterEditor** mod listed under _Suggested Mods_. Future versions _might_ include a way to do so.

**Warning: Do _not_ make any modifications to existing `states` present in `SporeAppStates.txt`. Removing or modifying them may result in soft-locking and/or crashes.**

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
* Part Limit: Part limit increased to 1023 total parts (crashes if saved at 1024 parts exactly (exact cause unknown), and passed 1024 fails to load correctly after restarting the game).
* Budget and Complexity: The part budget and complexity budget have both been increased to 999,999, effectively eliminating any concern for part costs outside of modded parts with purposefully high costs.

## Handle Modifications
Due to the way Spore's Editors are programmed, Morph Handles, Rotation Rings, Rotation Balls, etc. are scaled proportional to the given Editor's boundary size. This present an issue, as while an Editor can be configured to use custom handles, the convoluted manner in which Rotation Rings are handled means that they cannot properly be configured specifically for this Editor, meaning that changes have to be applied globally. This has the unfortunate side effect of making Rotation Rings univerally smaller to accomodate hte Absurd Editor's increased boundaries, rendering them effectively useless in other editors so long as this mod is installed.

This may be fixed later, but may require scripting, in turn requiring the use of the Spore ModAPI Launcher Kit or Spore Mod Loader.

Additionally, a bug relating to Dark Injection causes Nudge (Square/Depth) Handles to be reset to their natural size. Seeing as barely any parts in the Vehicle / Building Editors use Nudge Handles, this rarely comes into play.

## Suggested Mods:
These mods are compatible with and expand on the Absurd Vehicle Editor, though not all add content to the AVE directly. Mods requiring the SMAPILK or SML are indicated with an `&`:
* (&) [EnterEditor](https://github.com/VanillaCold/SporeEnterEditor) by VanillaCold : Allows the user to access the Editor via the Cheat Console instead of being limited to only being able to run it from Command Line or Shortcuts. It can also be used to open Absurd Vehicles in any other Editor, including the UFO Editor. Doing this allows the user to access parts not directly available in the AVE, but in normal versions of the Vehicle Editor. The ID of the AVE is `vehicleabsurd`, therefor the command would be `entereditor vehicleabsurd` or `editcreation vehicleabsurd`.
* [The Means of Production](https://mega.nz/file/TMF3TLjC#-6n4fzY6hbNE-oO_jRFEl0du5D8IGEVfe6Kaqnnx0yI) by vainglory : Adds every category of part to every Vehicle Editor - including the UFO Editor. Additionally, adds non-animating and effect-less duplicates of every relevant part.
* [BioTech Parts](https://www.mediafire.com/file/n47frrzn5ppfo9h/BioTech_Parts.package/file) by mx3brainpower and Lord Tenebris : Adds most Creature Editor Parts to the Vehicle Editors, including animations. Abandoned project, some parts have not been completely ported in a polished state. **Warning: beware ads on MediaFire pages**.
* [Port and Starboard](https://github.com/Valla-Chan/Spore-Mods/releases/tag/SporePortAndStarbord) by Valla-Chan : Adds duplicates of the Vehicle Editor cockpits and chassis that function as detail parts, allowing you to place them on the sides of vehicles. Useful for sidestepping issues with Building Editor mechanics being used on those parts.
* (&) [Wordsmith](https://github.com/Valla-Chan/Spore-Mods/releases/tag/SporeMod) by Valla-Chan : Adds letters from the Latin, Hiragana, and Katakana alphabets, as well as numbers and a few symbols, into the Vehicle (and Building) editors.
* [Building & Vehicle Fusion](https://davoonline.com/phpBB3/viewtopic.php?f=118&t=5021) by mx3brainpower : Adds all vanilla Vehicle Parts into the Building Editor's palette and vice-versa.
* (&) [Cheatbox](https://github.com/MADPSI/Cheatbox) by MADPSI : An extensive collection of cheats and keybinds that expands the functions of the Editors. Includes a cheat and bind for panning the camera and creating a placement grid, both available in the AVE.

## Acknowledgements
* [Splitwirez](https://github.com/Splitwirez) : Early developement assistance.
* [ACyborgSquid](https://www.instagram.com/aaron_debney?igsh=MWJ0b251bzE1dnI1aw==) (MythicalMist) : _Extensive_ beta testing, troubleshooting and public representation.
* All above mentioned suggested mod makers.
* [DarkEdgeTV](https://x.com/DarkEdgeTV) : _Indirect_ suggestions.
* [VanillaCold](https://github.com/VanillaCold) : AVE inspired by [Advanced CE](https://github.com/VanillaCold/Spore-AdvancedCE) mod.

## Made with the Absurdifier
### Salgan Rupture-class Destroyer (MythicalMist)
![image](https://github.com/user-attachments/assets/a9f0bc60-dc20-4ae3-b386-630d2e8624e4)

### Angel Cult War Balloon (MythicalMist)
![image](https://github.com/user-attachments/assets/7b30c4da-ac5c-4534-9836-6e4fba4279db)

### Angel Cult Mobile Church (MythicalMist)
![image](https://github.com/user-attachments/assets/1f7f6b8b-8460-48dd-b992-43e4c023b1a2)

### Angel Cult Mobile Pyre (MythicalMist)
![image](https://github.com/user-attachments/assets/6c379bce-7943-4539-86a2-8b2f47c3ef42)

### Angel Cult Crusade Buggy (MythicalMist)
![image](https://github.com/user-attachments/assets/4fac3ef5-bd68-476f-9ddc-50bf91a568c0)

### Decumarian Crusader (MythicalMist)
![image](https://github.com/user-attachments/assets/ea6806b1-db1d-46db-a37a-ee02fbf17e68)

### Decumarian Communion Shrine (MythicalMist)
![image](https://github.com/user-attachments/assets/21755e5e-4b31-415e-bed8-af0e3ae17ab9)

### Salgan Attack Vessel (MythicalMist)
![image](https://github.com/user-attachments/assets/97802c26-7ecf-4a5d-b97c-4f32cb5b9802)

### Deco Building (MythicalMist)
![image](https://github.com/user-attachments/assets/50c6a80c-bd81-4074-a8f2-a4d06df5bfa8)

### Futuristic Laser Cannon Cruiser (MythicalMist)
![image](https://github.com/user-attachments/assets/512fed81-91f9-405a-8edf-085d449fb33e)

### Super Planetbuster Laser Platform (MythicalMist)
![image](https://github.com/user-attachments/assets/5d7b0582-4c44-427d-8444-6514c89c2972)

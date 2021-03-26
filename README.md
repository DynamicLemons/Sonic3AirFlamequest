# Sonic3FlameQuestRepo
Sonic 3 Flame Quest is a mod for Sonic the Hedgehog 3: Angel Island Revisited by Sega/Eukaryot. It's a pseudo sequel to the ROM hack Sonic Scorched Quest, incorporating many of its ideas but with a Sonic 3 (AIR) twist. Experience a new adventure through the flaming landscapes of Angel Island as Sonic & co. attempt to stop Robotnik from getting his hands on the Flame Emeralds!

### Features: ###
* Custom Bosses
* Redesigned Levels
* New Soundtrack
* New stage gimmicks
* Metal Sonic
* Easter Eggs
* Et cetera

### MOST (IF NOT ALL) THIS STUFF SHOULD BE PORTED TO THEIR OWN SEPARATE ISSUES (except the code quality guidelines, those can stay here) ###

### Code Quality Guidelines ###
As the Code QA guy, I'd like to propose some general guidelines to ensure code quality:
 * Comments should be used so that code is easier to understand (would make adding to/modifying each others' code much easier)
      * Comments should be placed before functions explaining their purpose or what's been modified within them. 
 * Code should be formatted properly:
      * Code should be properly indented
      * Local variable names should use `camelCase`
      * Defines should be in all caps (minus the prefix), separating each word with an underscore (e.g. `FlameQuest.DEFINE_EXAMPLE_VARIABLE`)
      * Variable names should be descriptive of their purpose (e.g. `playerOneStartPosX` for a variable that stores the first player’s starting position)
           * Variable names should be as short as possible while doing this. Descriptiveness should be prioritized over length.
 * **All** global variables, defines, and function names should start with `FlameQuest.` 
      * For specific categories of variables, an additional prefix might be necessary (e.g. `FlameQuest.Setting.`, `FlameQuest.Secret.`, etc.)
      * This is not necessary for local variables.
 * Defines & Global Variables should be defined at the top of the document they’re in. Defines should be defined in their own file in the defines folder, with the file name preceded by `defines_`. ~~Global variables should probably also be defined this way, but until we decide to separate them into their own file(s) they should be placed at the top of their respective documents. Global variables that would be used in various places throughout the mod should be defined in their own files regardless.~~
      * Unless there are any oppositions, global variables should be defined in their own files from now own, similarly to defines. They can either go in their own file (`defines_global`) or their own file(s) (`global_` or `globals_`) depending on how we want to organize things (I'd personally go with `globals_`,  and have each file be purpose-oriented).
 * No obfuscation (if it's necessary, stuff can be obfuscated for public builds, but internal builds should remain unobfuscated)
 * Files should be organized properly (e.g. all the bosses would go in a folder each in their own `.lemon files`, `main.lemon` would include stuff like `Init()`, etc.)
      * Each change doesn't necessarily need to be in its own file (this relies a lot on judgement and is kinda hard to explain).
      * This is also true of sprites, audio files, rawdata & levels wherever possible.
 * Wherever possible, calling the `base.` version of functions should be preferred over overwriting vanilla functions.
 * The mod should not require a preview version of the game. This means that no preview version specific features should be added in the `master` branch.
      * Preview-specific things can be added in their own branch(es) for when the preview version eventually goes stable.
 * Misc stuff:
      * The conditions in `if` statements should be enclosed within parentheses (e.g. `if ((conditionOne && conditionTwo) || (conditionThree || conditionFour))`)
           * This is how if statements must be formatted in other coding languages (such as Java, C/C++, etc.) and should probably be carried over to Lemon script as well

I do plan on doing all this myself at some point (preferably not before the mod's final release), but it'd be better if new code was made with these guidelines in mind.
	~Code Quality Assurance Guy (DaKingofCheckerz)


### Easter Egg/Misc Ideas ###
* If we do go with Oil Desert Zone music, ducking for three minutes causes the theme to switch to ODZ 2
* “Press B to chuckle”
* RGB Knux
* Easter egg zone names
* Ice Capn’t (Triggered by a data select code)
* Messing around with the sound test will show images based on the entered code, like Sonic CD.


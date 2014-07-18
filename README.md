Chatterer
=========

A plugin for Kerbal Space Program which adds some SSTV, beeps, and nonsensical radio chatter between your crewed command pods and Mission Control.

Changelog:

v0.5.9.4:
- Recompiled for KSP v0.24 (First Contracts)
- Fixed chatter volume resetting @80% on awake (finally)

v0.5.9.3: 
- Recompiled for KSP v0.23.5 (fixes missing Airlock/Breath sounds)
- Added Debug Mode setting (disabled by default, so Chatterer no more spam your Log)
- Disabled "Remotech integration" & "Check for update" settings as they don't work (for now)

v0.5.9.2:
- Made integration with blizzy78's Toolbar plugin optional (will use Chatterer default icon if toolbar plugin is not installed)

v0.5.9:
- Recompiled with 0.23 references
- integration with blizzy78's Toolbar plugin
- enabled airlock sound when going to and from EVA
- Skin management : Using 'Resources.FindObjectsOfTypeAll' instead of 'FindObjectsOfTypeIncludingAssets' [obsolete with new Unity version]
- replaced "Mute" button by "Close UI window" button (Mute is causing NullRefEx spam for now)
- removed feedback sound filter option [Unity :Obsolete("feedback is deprecated, this property does nothing.")]

v.0.5.8 [16 Nov]
- Added atmospheric wind that fades in/out according to atmospheric density. Code and idea from Real Space Environment
- Different breathing sound. Slightly louder. Loud enough?
- Soundscapes are an optional download here [ soundscape.zip ] (35MB)
- In the .zip is a soundscape folder. Extract and copy folder to GameData/Chatterer/Sounds/AAE/
- Other new sounds (EVA breathing, vessel background hum, wind) can also be removed; or just remove the entire AAE folder

v.0.5.7 [10 Nov]
- New audio:
* EVA breathing from the Real Space Environment mod has been added. Many thanks to jeti140973
* 35 random soundscapes can be played back-to-back or on a timer
* Two background players to loop ambient vessel sounds
* 14 new beep samples (beep samples from previous versions are no longer included!)
- Cleaned up the UI by hiding less important things behind a new Settings toggle "Show Advanced Options"

v.0.5.6
- Fixed EVA Kerbals from triggering auto-chatter when jumping around
- Fixed main window from showing up when it should be hidden
- Fixed lots of path and ConfigNode problems. Thanks to Gristle, MainSailor, jrandom, BigFatStupidHead, and #kspmodders for the help!
- Lots of audio loading changes thanks to the lifting of the ban on System.IO:
* Can now load any of the Unity supported audio formats (wav, aif, ogg, mp3)
* No more limit on the number of clips to try to load
* Audio files no longer have to conform to a naming pattern to be loaded by the plugin
* Since names don't matter anymore, chatter, sstv, and probe audio files now have subfolders inside /Chatterer/Sounds
- Added individual vessel settings
- Added some tooltips (Thanks to Protractor source)
- Added chorus, distortion, echo, highpass, lowpass, and reverb filters to chatter and beeps
- Added buttons to return filters to default settings
- Added unlimited beep sources
- Config files now saved as ConfigNodes
- Fixed SSTV image slant
- ElectricCharge usage can be toggled on/off in settings
- Added a couple new skins from the AssetBase
- Fixed 'Allow update check' toggle and insta-SSTV key change from being hidden on crewless vessels
- Changed beep name/number to a button that plays the selected clip once
- Fixed skinned buttons displaying when No Skin is selected

v.0.5 [3 Jul]
- Now using part-free KSPAddon method instead of PartModule
- Added SSTV transmissions
- Increased number of beepers to three
- Beep timing can be toggled between precise and loose
- Beeps can be looped
- Beep clip can be set to random
- GUI split into sections and slider size decreased
- Icon can be relocated anywhere on the screen
- Removed unnecessary directories from Sounds and Textures
- Changed beep pitch display to a percentage
- Config read/write rewritten to be more sensible
- Fixed 'Load' button to not load already loaded dirs and not accept 'directory name'
- Fixed issues with skins sometimes displaying incorrectly
- Added a toggle to disable beeps during chatter
- Added a toggle to allow http update checks

v.0.4.1 [1 Jun]
- Added a set of kerbalized Russian chatter
- No more .cfg editing for adding custom audio, now added in game
- Stopped power usage when chatter/beep frequency is off
- Stopped event chatter when chatter frequency is off
- Added a button to swap between probe and chatter mode
- Fixed empty audiosets from breaking the plugin
- Cleaned up AudioSources and AudioClip array
- Icon textures load from game database

v.0.4 [26 May]
- Plugin files moved to use the new game database
- Create and play your own chatter sets (see README file for instructions)
- Added a new STS-1 chatter set
- Added new probe beeps
- Added optional RemoteTech integration to suspend or delay radio chatter
- Quindar tones are now toggleable and have a volume control
- Now uses a small amount of ElectricCharge (0.025/s)
- Added some other skin choices

v.0.3.2 [22 Mar]
- Added a second, stylish radial Radio part courtesy of baalzebob
- Rescaled the first part in cfg to make it more manageable (Thanks Kreuzung)
- Part checks via http for a newer version on flight start
- Insta-chatter key now saves and loads (Thanks Mu)
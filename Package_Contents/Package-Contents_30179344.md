Summary
=======

This section simply lists all of the contents of the package, denoting non-mission critical package content as optional.

Required Content
================

These items are a must for Amplifi to operate properly out-of-the-box.

*   Amplifi Engine prefab used to create “Amplifi Engine” scene objects.
    
*   Amplifi Node prefab used to create “Amplifi Node” scene objects.
    
*   Scripts directory containing the Amplifi Engine backend code.
    

Optional Content
================

Items marked as optional will be explained below as to why these items are considered optional. Most of the available optional items are provided to simplify the Amplifi onboarding process.

_These items are considered optional because they are not required for Amplifi to run but are provided simply to ease customer onboarding._

*   pre-built/example Amplifi Context objects.
    
    *   1x SFX AmplifiContext Scriptable Object
        
    *   1x Ambience AmplifiContext Scriptable Objects
        
    *   1x Music AmplifiContext Scriptable Objects
        

_These items are considered optional because they are not required for Amplifi to run but are provided so developers lacking audio files can quickly test Amplifi in their scene with temporary audio files._

*   Free Sample AudioClip's.
    
    *   4x Sample Ambience
    *   4x Sample Music            
    *   4x Sample SFX

_This item is considered optional because it is not required for Amplifi to run. Developers can simply create their own AudioMixer/Snapshot/Groups from scratch if preferred._

*   pre-built/example AudioMixer.
    
    *   1x AudioMixer “Amplifi Mixer”
        
    *   1x AudioMixerSnapshot “Underwater”
        
    *   3x Provided AudioMixerGroup’s \[“Music“, “Ambience“, “SFX“\]
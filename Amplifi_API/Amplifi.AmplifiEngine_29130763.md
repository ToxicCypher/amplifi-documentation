Description
===========

### Summary

The `AmplifiEngine` class is designed to manage and control audio sources for ambience, sound effects, and music within a Unity project. It also supports and manages Audio Mixer groups and snapshots, providing a comprehensive audio management system.

This module is the gateway for all audio management related functionality. If music needs to transition, a sound effect needs to play, ambience needs to be invoked and/or an audio mixer snapshot needs to be blended, the function call will be originated here. Any further tasks needed to carry out any of these operations will be handled by AmplifiEngine on your behalf.    

Usage
=====

This section provides examples of how this class can be used programmatically.

```
using UnityEngine;
using Amplifi;

public class Example : MonoBehaviour
{
    [SerializeField] AudioMixerSnapshot snapshot;
    [SerializeField] AudioMixer mixer;

    void OnTriggerEnter(Collider other)
    {
      /* 
      * Access the AmplifiEngine in the current scene with the following syntax and
      * Programatically blend an AudioMixerSnapshot.
      */
      
      AmplifiEngine.Core.BlendSnapshot(mixer: mixer, snapshot: snapshot, duration: 1.0f)
    }
}
```

Properties
==========

<table data-table-width="1011" data-layout="default" data-local-id="f44e093b-2b44-4e99-9e6d-51bd712b2279" class="confluenceTable"><colgroup><col style="width: 190.0px;"><col style="width: 166.0px;"><col style="width: 195.0px;"><col style="width: 458.0px;"></colgroup><tbody><tr><th data-highlight-colour="var(--darkreader-bg--ds-background-accent-gray-subtlest, #1d2021)" class="confluenceTh"><p><strong>Property</strong></p></th><th data-highlight-colour="var(--darkreader-bg--ds-background-accent-gray-subtlest, #1d2021)" class="confluenceTh"><p><strong>Type</strong></p></th><th data-highlight-colour="var(--darkreader-bg--ds-background-accent-gray-subtlest, #1d2021)" class="confluenceTh"><p><strong>Default Value</strong></p></th><th data-highlight-colour="var(--darkreader-bg--ds-background-accent-gray-subtlest, #1d2021)" class="confluenceTh"><p><strong>Description</strong></p></th></tr><tr><td class="confluenceTd"><p>baseSnapshot</p></td><td class="confluenceTd"><p>AudioMixerSnapshot</p></td><td class="confluenceTd"><p>null</p></td><td class="confluenceTd"><p>The default AudioMixerSnapshot for the active scene.</p></td></tr><tr><td class="confluenceTd"><p>baseTrack</p></td><td class="confluenceTd"><p>AudioClip</p></td><td class="confluenceTd"><p>null</p></td><td class="confluenceTd"><p>The default AudioClip (Music Track) for the active scene. This AudioClip will be instantiated at run-time and will be reverted to unless otherwise specified when the current Music (Proximity) nodes is destroyed. This value may be null, resulting in silence.</p></td></tr><tr><td class="confluenceTd"><p>baseTrackContext</p></td><td class="confluenceTd"><p><a href="../Amplifi_Context_Configuration/Amplifi-Context-Configuration_29852062.md" data-linked-resource-id="29852062" data-linked-resource-version="3" data-linked-resource-type="page">AmplifiContext</a></p></td><td class="confluenceTd"><p>null</p></td><td class="confluenceTd"><p>The default AmplifiContext used to apply configuration to the default track.</p></td></tr><tr><td class="confluenceTd"><p>initialAudioEscalation</p></td><td class="confluenceTd"><p>float</p></td><td class="confluenceTd"><p>0</p></td><td class="confluenceTd"><p>The speed at which the base track volume is initially smoothed into its target volume.</p></td></tr><tr><td class="confluenceTd"><p>duplicateLimit</p></td><td class="confluenceTd"><p>int</p></td><td class="confluenceTd"><p>10</p></td><td class="confluenceTd"><p>Specifies the number of duplicate SFX clips of the same title that can be instanced at a time. For unlimited duplicates, set this value to 0.</p></td></tr></tbody></table>

Public Methods
==============

<table data-table-width="1011" data-layout="default" data-local-id="80a4ffbb-fe8b-4f9c-a958-2b03d75504b9" class="confluenceTable"><colgroup><col style="width: 214.0px;"><col style="width: 188.0px;"><col style="width: 607.0px;"></colgroup><tbody><tr><th class="confluenceTh"><p><strong>Function</strong></p></th><th class="confluenceTh"><p><strong>Return Type</strong></p></th><th class="confluenceTh"><p><strong>Description</strong></p></th></tr><tr><td class="confluenceTd"><p>InvokeSoundEffect</p></td><td class="confluenceTd"><p>void</p></td><td class="confluenceTd"><p>Generates a single sound effect instance which will self-manage its lifecycle, destroying the instanced SFX when the sound effect is over.</p></td></tr><tr><td class="confluenceTd"><p>InvokeLoopingSoundEffect</p></td><td class="confluenceTd"><p>GameObject</p></td><td class="confluenceTd"><p>Generates a single sound effect instance on a loop. This SFX will not stop playing until a specified game object has exited the bounding volume of the origin SFX node.</p></td></tr><tr><td class="confluenceTd"><p>EnableAmbience</p></td><td class="confluenceTd"><p>void</p></td><td class="confluenceTd"><p>Enables ambience audio tied to a specific node.</p></td></tr><tr><td class="confluenceTd"><p>UpdateMusic</p></td><td class="confluenceTd"><p>AudioClip</p></td><td class="confluenceTd"><p>Transitions between music tracks.</p></td></tr><tr><td class="confluenceTd"><p>BlendSnapshot</p></td><td class="confluenceTd"><p>void</p></td><td class="confluenceTd"><p>Blends audio snapshots for smooth transitions between audio states.</p></td></tr><tr><td class="confluenceTd"><p>GetAudioSourceRegistry</p></td><td class="confluenceTd"><p><a href="../Amplifi_API/Support_Modules/Concrete_Classes/AudioSourceRegistry_29163541.md" data-linked-resource-id="29163541" data-linked-resource-version="2" data-linked-resource-type="page">AudioSourceRegistry</a></p></td><td class="confluenceTd"><p>Access to audio source register through a getter method.</p></td></tr><tr><td class="confluenceTd"><p>GetSoundEffectRegistry</p></td><td class="confluenceTd"><p><a href="../Amplifi_API/Support_Modules/Concrete_Classes/SoundEffectRegistry_29098056.md" data-linked-resource-id="29098056" data-linked-resource-version="2" data-linked-resource-type="page">SoundEffectRegistry</a></p></td><td class="confluenceTd"><p>Access to sound effect register through a getter method.</p></td></tr><tr><td class="confluenceTd"><p>GetCoroutineRegistry</p></td><td class="confluenceTd"><p><a href="../Amplifi_API/Support_Modules/Concrete_Classes/CoroutineRegistry_29098016.md" rel="nofollow">CoroutineRegistry</a></p></td><td class="confluenceTd"><p>Access to coroutine register through a getter method.</p></td></tr></tbody></table>

Delegates
=========

<table data-table-width="1011" data-layout="default" data-local-id="89784fef-e68c-4e61-b6fc-544d6911d851" class="confluenceTable"><colgroup><col style="width: 199.0px;"><col style="width: 810.0px;"></colgroup><tbody><tr><th class="confluenceTh"><p><strong>Delegate Title</strong></p></th><th class="confluenceTh"><p><strong>Triggering Event</strong></p></th></tr><tr><td class="confluenceTd"><p>OnAmbienceEnabled</p></td><td class="confluenceTd"><p>This delegate is triggered when the EnableAmbience function is called.</p></td></tr><tr><td class="confluenceTd"><p>OnMusicTransition</p></td><td class="confluenceTd"><p>This delegate is triggered when the UpdateMusic function is called.</p></td></tr><tr><td class="confluenceTd"><p>OnSoundEffectGenerated</p></td><td class="confluenceTd"><p>This delegate is triggered when the InvokeLoopingSoundEffect function or the InvokeSoundEffect function is called.</p></td></tr><tr><td class="confluenceTd"><p>OnSnapshotBlend</p></td><td class="confluenceTd"><p>This delegate is triggered when the BlendSnapshot function is called.</p></td></tr></tbody></table>
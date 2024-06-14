Description
===========

### Summary

The `AmplifiControlTower` class is a static utility designed to manage the lifecycle of audio sources in a Unity project. It includes functionality to lock and unlock audio source creation, preventing new audio sources from being instantiated when locked as well as decommissioning logic for all AudioSources and Coroutines currently existing under the influence of `Amplifi`.

### Related Resources

*   [AmplifiEngine](Amplifi.AmplifiEngine_29130763.md)
    

Usage
=====

This section provides examples of how this class can be used programmatically.

```
using UnityEngine;
using Amplifi;

public class Example : MonoBehaviour
{    
    /* Based on some event (Cutscene trigger, scene exit, etc.). */
    void OnTriggerEnter(Collider other)
    {
      /* Perform an Amplifi decomission. */
      AmplifiControlTower.Decomission(duration: 1.0f);
    }
}
```

Static Methods
==============

<table data-table-width="1011" data-layout="default" data-local-id="73d1f227-5be8-4160-bb51-e321f482d5c9" class="confluenceTable"><colgroup><col style="width: 243.0px;"><col style="width: 223.0px;"><col style="width: 542.0px;"></colgroup><tbody><tr><th class="confluenceTh"><p><strong>Function</strong></p></th><th class="confluenceTh"><p><strong>Return Type</strong></p></th><th class="confluenceTh"><p><strong>Description</strong></p></th></tr><tr><td class="confluenceTd"><p>BlockAudioSourceCreation</p></td><td class="confluenceTd"><p>void</p></td><td class="confluenceTd"><p>This method locks audio source creation via the AmplifiEngine.</p></td></tr><tr><td class="confluenceTd"><p>UnBlockAudioSourceCreation</p></td><td class="confluenceTd"><p>void</p></td><td class="confluenceTd"><p>This method unlocks audio source creation via the AmplifiEngine.</p></td></tr><tr><td class="confluenceTd"><p>IsLocked</p></td><td class="confluenceTd"><p>bool</p></td><td class="confluenceTd"><p>This method checks if audio source creation is currently locked. If audio source creation is locked, true is returned, else false is returned.</p></td></tr><tr><td class="confluenceTd"><p>RebuildAmplifiConfiguration</p></td><td class="confluenceTd"><p>void</p></td><td class="confluenceTd"><p>Rebuild the AmplifiConfig object that is current being used by Amplifi Engine. This provides a way to update the default track, default track context, default snapshot, initial escalation duration and SFX duplicate limit values at run-time.</p></td></tr><tr><td class="confluenceTd"><p>RestartEngine</p></td><td class="confluenceTd"><p>void</p></td><td class="confluenceTd"><p>This method initiates a shutdown process for all audio sources over a specified duration. It stops ongoing Amplifi-related coroutines, and gradually reduces the volume of all active audio sources all without locking the engine from creating new audio sources with Amplifi.</p></td></tr><tr><td class="confluenceTd"><p>Decomission</p></td><td class="confluenceTd"><p>void</p></td><td class="confluenceTd"><p>This method initiates a shutdown process for all audio sources over a specified duration. It locks audio source creation, stops ongoing Amplifi-related coroutines, and gradually reduces the volume of all active audio sources.</p></td></tr><tr><td class="confluenceTd"><p>DecomissionAudioSources</p></td><td class="confluenceTd"><p>void</p></td><td class="confluenceTd"><p>This method stops all AudioSource components registered with the Amplifi engine.</p></td></tr><tr><td class="confluenceTd"><p>StopAmplifiCoroutines</p></td><td class="confluenceTd"><p>void</p></td><td class="confluenceTd"><p>This method stops all coroutines registered with the Amplifi engine.</p></td></tr></tbody></table>

Delegates
=========

<table data-table-width="1011" data-layout="default" data-local-id="89784fef-e68c-4e61-b6fc-544d6911d851" class="confluenceTable"><colgroup><col style="width: 230.0px;"><col style="width: 780.0px;"></colgroup><tbody><tr><th class="confluenceTh"><p><strong>Delegate Title</strong></p></th><th class="confluenceTh"><p><strong>Triggering Event</strong></p></th></tr><tr><td class="confluenceTd"><p>OnEngineRestart</p></td><td class="confluenceTd"><p>This delegate is triggered when the RestartEngine function is called.</p></td></tr><tr><td class="confluenceTd"><p>OnEngineDecomission</p></td><td class="confluenceTd"><p>This delegate is triggered when the Decomission function is called.</p></td></tr><tr><td class="confluenceTd"><p>OnEngineLock</p></td><td class="confluenceTd"><p>This delegate is triggered when the BlockAudioSourceCreation function is called.</p></td></tr><tr><td class="confluenceTd"><p>OnEngineUnlock</p></td><td class="confluenceTd"><p>This delegate is triggered when the UnBlockAudioSourceCreation function is called.</p></td></tr></tbody></table>
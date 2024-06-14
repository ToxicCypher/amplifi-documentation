Description
===========

### Summary

The `AmplifiMixerSupport` class is a utility class that provides methods to retrieve `AudioMixer`, `AudioMixerGroup`, and `AudioMixerSnapshot` objects by name.

Usage
=====

This section provides examples of how this class can be used programmatically.

```
using UnityEngine;
using Amplifi;

public class Example : MonoBehaviour
{
    /* Declare each of the mixer related items we can look up with this module. */
    private AudioMixer mixer;
    private AudioMixerGroup group;
    private AudioMixerSnapshot snapshot;
    
    /* Declare a new AmplifiContext object. */
    private AmplifiContext context;
    
    void Start() 
    {
      mixer = AmplifiMixerSupport.GetAudioMixerByName("Example Audio Mixer");
      group = AmplifiMixerSupport.GetAudioMixerGroupByName(mixer, "Example Mixer Group")
      snapshot = AmplifiMixerSupport.GetAudioMixerSnapshotByName(mixer, "Example Mixer Snapshot")
      
      /* Instance an AmplifiContext object, supplying an AudioMixerGroup */
      context = AmplifiContext.CreateInstance(mixerGroup: group);
    }

    void OnTriggerEnter(Collider other)
    {
      /* Blend the AudioMixer and AudioMixerSnapshot we looked up. */
      AmplifiEngine.Core.BlendSnapshot(mixer: mixer, snapshot: snapshot, duration: 1.0f)
  
    }
}
```

Static Methods
==============

<table data-table-width="1011" data-layout="default" data-local-id="3b885194-feb5-43e8-a6a2-bd2c990acd5d" class="confluenceTable"><colgroup><col style="width: 250.0px;"><col style="width: 268.0px;"><col style="width: 490.0px;"></colgroup><tbody><tr><th class="confluenceTh"><p><strong>Function</strong></p></th><th class="confluenceTh"><p><strong>Return Type</strong></p></th><th class="confluenceTh"><p><strong>Description</strong></p></th></tr><tr><td class="confluenceTd"><p>GetAudioMixerByName</p></td><td class="confluenceTd"><p>AudioMixer</p></td><td class="confluenceTd"><p>Performs a lookup of an AudioMixer using a string pattern, in your project. The AudioMixer must exist in a ‘Resources’ directory in-order for it to be found with this function as it utilizes the <strong>UnityEngine.Resources</strong> class.</p></td></tr><tr><td class="confluenceTd"><p>GetAudioMixerGroupByName</p></td><td class="confluenceTd"><p>AudioMixerGroup</p></td><td class="confluenceTd"><p>Performs a lookup of an AudioMixerGroup using a target AudioMixer and a string pattern for the desired AudioMixerGroup, in your project.</p></td></tr><tr><td class="confluenceTd"><p>GetAudioMixerSnapshotByName</p></td><td class="confluenceTd"><p>AudioMixerSnapshot</p></td><td class="confluenceTd"><p>Performs a lookup of an AudioMixerSnapshot using a target AudioMixer and a string pattern for the desired AudioMixerSnapshot, in your project.</p></td></tr></tbody></table>
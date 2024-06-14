Summary
=======

In this section, you will learn about all of the configuration that is available for Utility Amplifi Nodes and in general, how each Utility Amplifi Node subtype behaves.

Utility Node Subtype Behavior
=============================

Below is a table detailing all of the available Utility node subtypes and a detailed description regarding the general behavior of the Utility node subtypes.

<table data-table-width="760" data-layout="default" data-local-id="01534237-8e2b-4033-aa0e-d4e382a8d681" class="confluenceTable"><colgroup><col style="width: 160.0px;"><col style="width: 599.0px;"></colgroup><tbody><tr><th class="confluenceTh"><p><strong>Node Subtype</strong></p></th><th class="confluenceTh"><p><strong>Description</strong></p></th></tr><tr><td class="confluenceTd"><p>DecomissionAudio</p></td><td class="confluenceTd"><p>Initiates a shutdown process for all audio sources over a specified duration. It locks audio source creation, stops ongoing Amplifi-related coroutines, and gradually reduces the volume of all active audio sources.</p></td></tr><tr><td class="confluenceTd"><p>RestartEngine</p></td><td class="confluenceTd"><p>Initiates a shutdown process for all audio sources over a specified duration. It stops ongoing Amplifi-related coroutines, and gradually reduces the volume of all active audio sources all without locking the engine from creating new audio sources with Amplifi.</p></td></tr><tr><td class="confluenceTd"><p>LockEngine</p></td><td class="confluenceTd"><p>Locks audio source creation via the AmplifiEngine.</p></td></tr><tr><td class="confluenceTd"><p>UnlockEngine</p></td><td class="confluenceTd"><p>Unlocks audio source creation via the AmplifiEngine.</p></td></tr></tbody></table>

Utility Node Configuration
==========================

Below is a table detailing all of the available configuration for the Utility type Amplifi Node. If any Utility Amplifi Node subtypes are available, the availability of a given parameter for a particular subtype will be noted.

<table data-table-width="1373" data-layout="default" data-local-id="932f4727-a3f6-428f-8ae5-ce617ba4b772" class="confluenceTable"><colgroup><col style="width: 236.0px;"><col style="width: 180.0px;"><col style="width: 159.0px;"><col style="width: 232.0px;"><col style="width: 557.0px;"></colgroup><tbody><tr><th class="confluenceTh"><p><strong>Parameter</strong></p></th><th class="confluenceTh"><p><strong>Data Type</strong></p></th><th class="confluenceTh"><p><strong>Default Value</strong></p></th><th class="confluenceTh"><p><strong>Subtype Availability</strong></p></th><th class="confluenceTh"><p><strong>Description</strong></p></th></tr><tr><td class="confluenceTd"><p>Decommission Duration</p></td><td class="confluenceTd"><p>float</p></td><td class="confluenceTd"><p>0.0f</p></td><td class="confluenceTd"><p>DecomissionAudio, RestartEngine</p></td><td class="confluenceTd"><p>The length of time in seconds that it will take to reduce the volume of all active AudioSources to 0.0f.</p></td></tr><tr><td class="confluenceTd"><p>Single Use</p></td><td class="confluenceTd"><p>bool</p></td><td class="confluenceTd"><p>false</p></td><td class="confluenceTd"><p>DecomissionAudio, RestartEngine, LockEngine, Unlock Engine</p></td><td class="confluenceTd"><p>If true, when the associated node is triggered, it will be destroyed.</p></td></tr><tr><td class="confluenceTd"><p>Allowed Tags</p></td><td class="confluenceTd"><p>List&lt;string&gt;</p></td><td class="confluenceTd"><p>List&lt;string&gt; { }</p></td><td class="confluenceTd"><p>DecomissionAudio, RestartEngine, LockEngine, Unlock Engine</p></td><td class="confluenceTd"><p>A list of tags that are allowed to trigger this node, given that the game object that enters the bounding volume is tagged with one of the tags supplied to this list. If no tags are specified, any game object can trigger the target node.</p></td></tr></tbody></table>
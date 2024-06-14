### Summary

This option is only available to the SFX [AmplifiContext](Amplifi.AmplifiContext_29097985.md) type.

The `UtilitySubNodeType` enum within the `Amplifi` namespace defines different types of actions that a Utility type node can have within the Amplifi system.

### Options

<table data-table-width="760" data-layout="default" data-local-id="7dea2fae-7afd-462d-bf9b-7ee1577014ef" class="confluenceTable"><colgroup><col style="width: 221.0px;"><col style="width: 538.0px;"></colgroup><tbody><tr><th class="confluenceTh"><p><strong>Option</strong></p></th><th class="confluenceTh"><p><strong>Definition</strong></p></th></tr><tr><td class="confluenceTd"><p>DecomissionAudio</p></td><td class="confluenceTd"><p>This method blocks the creation of new audio sources, stops all active Amplifi coroutines, and fades out existing audio sources over the specified duration.</p></td></tr><tr><td class="confluenceTd"><p>RestartEngine</p></td><td class="confluenceTd"><p>Restarts the audio engine by decommissioning existing audio sources and then unblocking new audio source creation without blocking future audio source creation via Amplifi.</p></td></tr><tr><td class="confluenceTd"><p>LockEngine</p></td><td class="confluenceTd"><p>Blocks the creation of new audio sources.</p></td></tr><tr><td class="confluenceTd"><p>UnlockEngine</p></td><td class="confluenceTd"><p>Unblocks the creation of new audio sources</p></td></tr></tbody></table>
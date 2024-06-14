### Summary

This option is only available to the SFX [AmplifiContext](Amplifi.AmplifiContext_29097985.md) type.

The `SFXSubNodeType` enum within the `Amplifi` namespace defines different types of relationships that a sound effects (SFX) node can have within the Amplifi system.

### Options

<table data-table-width="760" data-layout="default" data-local-id="7dea2fae-7afd-462d-bf9b-7ee1577014ef" class="confluenceTable"><colgroup><col style="width: 221.0px;"><col style="width: 538.0px;"></colgroup><tbody><tr><th class="confluenceTh"><p><strong>Option</strong></p></th><th class="confluenceTh"><p><strong>Definition</strong></p></th></tr><tr><td class="confluenceTd"><p>Orphan</p></td><td class="confluenceTd"><p>Spawns the instance SFX at the location of the triggered node but does not parent the instance SFX to the node.</p></td></tr><tr><td class="confluenceTd"><p>ChildOfOther</p></td><td class="confluenceTd"><p>Spawns the instance SFX at the location of the game object that triggered the SFX node, as a child of the game object that triggered the SFX node.</p></td></tr><tr><td class="confluenceTd"><p>ChildOfNode</p></td><td class="confluenceTd"><p>Spawns the instance SFX at the location of the triggered node and parents the instanced SFX to the related node.</p></td></tr></tbody></table>
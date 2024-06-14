Introduction
============

In this section, you will be guided through setting up the Amplifi Engine via the Unity Editor.

What is Amplifi Engine?
=======================

This object is a singleton, only one Amplifi Engine may exist at any given time within the active scene.

Amplifi Engine is the core of Amplifi and is required in your scene for Amplifi to operate. Amplifi Engine manages all Amplifi backend functionality so you don’t have to!

Creating Amplifi Engine
=======================

For examples on how to create AmplifiEngine via the Amplifi API, visit [Amplifi.AmplifiEngine](../Amplifi_API/Amplifi.AmplifiEngine_29130763.md).

### Creating the Amplifi Engine

_This section assumes that the current scene does not yet contain an Amplifi Engine game object._

1.  To add the “Amplifi Engine” to your scene, open the GameObject menu, however you might prefer, and select ‘Amplifi’ > ‘Amplifi Engine’. <br>
![image-20240609-000607.png](../docutils/attachments/30474242/30146980.png)
    
2.  At this time, the Amplifi Engine is ready to be configured. <br>
![image-20240609-000707.png](../docutils/attachments/30474242/29852223.png)
    

### Configuring the Amplifi Engine

Now it is time to configure the Amplifi Engine object that you have just created. Below is a table, describing each available parameter.

<table data-table-width="1011" data-layout="default" data-local-id="f44e093b-2b44-4e99-9e6d-51bd712b2279" class="confluenceTable"><colgroup><col style="width: 190.0px;"><col style="width: 166.0px;"><col style="width: 195.0px;"><col style="width: 458.0px;"></colgroup><tbody><tr><th data-highlight-colour="var(--darkreader-bg--ds-background-accent-gray-subtlest, #1d2021)" class="confluenceTh"><p><strong>Property</strong></p></th><th data-highlight-colour="var(--darkreader-bg--ds-background-accent-gray-subtlest, #1d2021)" class="confluenceTh"><p><strong>Type</strong></p></th><th data-highlight-colour="var(--darkreader-bg--ds-background-accent-gray-subtlest, #1d2021)" class="confluenceTh"><p><strong>Default Value</strong></p></th><th data-highlight-colour="var(--darkreader-bg--ds-background-accent-gray-subtlest, #1d2021)" class="confluenceTh"><p><strong>Description</strong></p></th></tr><tr><td class="confluenceTd"><p>Default Snapshot</p></td><td class="confluenceTd"><p>AudioMixerSnapshot</p></td><td class="confluenceTd"><p>null</p></td><td class="confluenceTd"><p>The default AudioMixerSnapshot for the active scene.</p></td></tr><tr><td class="confluenceTd"><p>Default Music</p></td><td class="confluenceTd"><p>AudioClip</p></td><td class="confluenceTd"><p>null</p></td><td class="confluenceTd"><p>The default AudioClip (Music Track) for the active scene. This AudioClip will be instantiated at run-time and will be reverted to unless otherwise specified when the current Music (Proximity) nodes is destroyed. This value may be null, resulting in silence.</p></td></tr><tr><td class="confluenceTd"><p>Default Context</p></td><td class="confluenceTd"><p><a href="../Amplifi_Context_Configuration/Amplifi-Context-Configuration_29852062.md" data-linked-resource-id="29852062" data-linked-resource-version="3" data-linked-resource-type="page">AmplifiContext</a></p></td><td class="confluenceTd"><p>null</p></td><td class="confluenceTd"><p>The default AmplifiContext used to apply configuration to the default track.</p></td></tr><tr><td class="confluenceTd"><p>Initial Audio Escalation</p></td><td class="confluenceTd"><p>float</p></td><td class="confluenceTd"><p>0</p></td><td class="confluenceTd"><p>The speed at which the base track volume is initially smoothed into its target volume.</p></td></tr><tr><td class="confluenceTd"><p>SFX Duplicate Limit</p></td><td class="confluenceTd"><p>int</p></td><td class="confluenceTd"><p>10</p></td><td class="confluenceTd"><p>Specifies the number of duplicate SFX clips of the same title that can be instanced at a time. For unlimited duplicates, set this value to 0.</p></td></tr></tbody></table>
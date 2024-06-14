Accessing The Engine
====================

The Amplifi Engine is built upon a single singleton class AmplifiEngine. This singleton class contains the methods that are used to perform all audio generation and management code.

Because the AmplifiEngine is a singleton, there will only ever be one instance of the engine in the active scene. With this information in mind, in-order to access the active scenes AmplifiEngine programmatically, developers can use the following syntax.

```
using UnityEngine;
using Amplifi;

public class Example : MonoBehaviour
{
    void Start()
    {
      /* Acessing the active AmplifiEngine instance, assigning to 'core' for demonstration, this is not necessary outside of this demo. */
      AmplifiEngine reference = AmplifiEngine.Core;
    }
```

Assuming your scene already has an AmplifiEngine instance provided, accessing the engine core is as simple as writing the following code.

```
AmplifiEngine.Core.[Your desired function/property here.]
```

API Index
=========

All documentation provided in the table below describes and demonstrates how developers can leverage Amplifi to achieve their game development and audio management goals.

All internal modules are described in documentation under the [Support Modules](Support-Modules_28672003.md) section. As these classes are not outward accessible, limited documentation is provided beyond general descriptions of the purpose each module serves.

<table data-table-width="760" data-layout="default" data-local-id="18eb3fdb-166d-4465-9bf8-0718b3c96f0f" class="confluenceTable"><colgroup><col style="width: 399.0px;"><col style="width: 361.0px;"></colgroup><tbody><tr><th class="confluenceTh"><p><strong>Class</strong></p></th><th class="confluenceTh"><p><strong>Type</strong></p></th></tr><tr><td class="confluenceTd"><p><a href="Amplifi.AmplifiContext_29097985.md" data-linked-resource-id="29097985" data-linked-resource-version="14" data-linked-resource-type="page">AmplifiContext</a></p></td><td class="confluenceTd"><p>Scriptable Object</p></td></tr><tr><td class="confluenceTd"><p><a href="Amplifi.AmplifiControlTower_29130753.md" data-linked-resource-id="29130753" data-linked-resource-version="10" data-linked-resource-type="page">AmplifiControlTower</a></p></td><td class="confluenceTd"><p>Static Class</p></td></tr><tr><td class="confluenceTd"><p><a href="Amplifi.AmplifiEngine_29130763.md" data-linked-resource-id="29130763" data-linked-resource-version="13" data-linked-resource-type="page">AmplifiEngine</a></p></td><td class="confluenceTd"><p>Monobehavior</p></td></tr><tr><td class="confluenceTd"><p><a href="Amplifi.AmplifiMixerSupport_29130773.md" data-linked-resource-id="29130773" data-linked-resource-version="4" data-linked-resource-type="page">AmplifiMixerSupport</a></p></td><td class="confluenceTd"><p>Static Class</p></td></tr></tbody></table>
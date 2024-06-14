### Summary

The `AmplifiInsights` class, which inherits from MonoBehaviour, provides insights into the Amplifi system within Unity. It includes serialized fields for lists of registered sound effects, monitored audio sources, and active coroutines, each annotated with tooltips for clarity. In its `LateUpdate()` method, it updates these lists by fetching data from the corresponding registries within the Amplifi engine, converting them into strings for display purposes. This class serves as a monitoring tool, offering visibility into the current state of sound effects, audio sources, and coroutines within the Amplifi system during runtime.

### Usage

Attach the Amplifi Insights component to any game object in your active scene to view the currently active AudioSources and Coroutines that have been created by the Amplifi engine.

### Gallery

![image-20240607-221418.png](attachments/29163531/29786143.png?width=385)
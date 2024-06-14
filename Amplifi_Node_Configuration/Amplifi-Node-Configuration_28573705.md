Introduction
============

In this section, you will be guided through setting up Amplifi Node objects via the Unity Editor.

What is an Amplifi Node?
========================

An Amplifi Node is a game object which is tightly coupled with the Amplifi Engine. Each Amplifi Node acts as a front-end for Amplifi Audio Management with the use of Amplifi Node configuration and collision triggers. Amplifi Node’s are designed to work out-of-the-box with little to no configuration but supplemental configurations may be provided with ease, utilizing [Amplifi Context](../Amplifi_Context_Configuration/Amplifi-Context-Configuration_29852062.md) objects, along with [Amplifi Engine Configuration](../Amplifi_Engine_Configuration/Amplifi-Engine-Configuration_30474242.md) and Amplifi Node configuration detailed in this documents sub-pages.

Multiple Amplifi Node components can be used on a single game object, allowing for a single game object to perform a mixture of tasks with Amplifi.


Creating an Amplifi Node
========================

Amplifi Nodes are purely designed for front-end | no-code development. For visual guidance on standing up Amplifi Node’s visit the [Video Tutorials](../Video_Tutorial/Video-Tutorials_29884437.md) page.

### Creating Stand-Alone Amplifi Node

1.  To add the “Amplifi Node” to your scene, open the GameObject menu, however you might prefer, and select ‘Amplifi’ > ‘Amplifi Node’.
    
    1.  If an “Amplifi Engine” object is not already in your scene, one will be added for you.
        
2.  At this time, the Amplifi Node is ready to be configured.
    

### Adding Amplifi Node Components to Game Objects

1.  To add the “Amplifi Node” to an existing game object in your scene, focus the game object in your scene that you would like to add an “Amplifi Node” component to.
    
2.  Select the ‘Add Component’ button.
    
3.  Search for and select the “Amplifi Node” component.
    
4.  At this time, the Amplifi Node is ready to be configured.
    

### Configuring the Amplifi Node

Now it is time to configure the Amplifi Node object that you have just created. Amplifi Node’s come in a variety of base configurations as well as subtype configurations, which will be explored in each of the Amplifi Node type documentation. See below for the list of Amplifi Node base types.


**Documentation**

[Ambience Node](../Amplifi_Node_Configuration/Ambience-Node_28770351.md)

[Music Node](../Amplifi_Node_Configuration/Music-Node_28278804.md)

[SFX Node](../Amplifi_Node_Configuration/SFX-Node_28639274.md)

[Snapshot Node](../Amplifi_Node_Configuration/Snapshot-Node_28704810.md)

[Utility Node](../Amplifi_Node_Configuration/Utility-Node_30867468.md)

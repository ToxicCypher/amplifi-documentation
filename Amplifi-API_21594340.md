<!DOCTYPE html>
<html>
    <head>
        <title>Amplifi : Amplifi API</title>
        <link rel="stylesheet" href="styles/site.css" type="text/css" />
        <META http-equiv="Content-Type" content="text/html; charset=UTF-8">
    </head>

    <body class="theme-default aui-theme-default">
        <div id="page">
            <div id="main" class="aui-page-panel">
                <div id="main-header">
                    <div id="breadcrumb-section">
                        <ol id="breadcrumbs">
                            <li class="first">
                                <span><a href="index.html">Amplifi</a></span>
                            </li>
                                                    <li>
                                <span><a href="28344324.html">Amplifi [Home]</a></span>
                            </li>
                                                </ol>
                    </div>
                    <h1 id="title-heading" class="pagetitle">
                                                <span id="title-text">
                            Amplifi : Amplifi API
                        </span>
                    </h1>
                </div>

                <div id="content" class="view">
                    <div class="page-metadata">
                        
        
    
        
    
        
        
            Created by <span class='author'> Cameron Gibson</span>, last modified on Jun 08, 2024
                        </div>
                    <div id="main-content" class="wiki-content group">
                    <h1 id="AmplifiAPI-AccessingTheEngine">Accessing The Engine</h1><p>The Amplifi Engine is built upon a single singleton class AmplifiEngine. This singleton class contains the methods that are used to perform all audio generation and management code. </p><p>Because the AmplifiEngine is a singleton, there will only ever be one instance of the engine in the active scene. With this information in mind, in-order to access the active scenes AmplifiEngine programmatically, developers can use the following syntax.</p><div class="code panel pdl" style="border-width: 1px;"><div class="codeContent panelContent pdl">
<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: c#; gutter: false; theme: Confluence" data-theme="Confluence">using UnityEngine;
using Amplifi;

public class Example : MonoBehaviour
{
    void Start()
    {
      /* Acessing the active AmplifiEngine instance, assigning to &#39;core&#39; for demonstration, this is not necessary outside of this demo. */
      AmplifiEngine reference = AmplifiEngine.Core;
    }</pre>
</div></div><p /><p>Assuming your scene already has an AmplifiEngine instance provided, accessing the engine core is as simple as writing the following code.</p><div class="code panel pdl" style="border-width: 1px;"><div class="codeContent panelContent pdl">
<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: c#; gutter: false; theme: Confluence" data-theme="Confluence">AmplifiEngine.Core.[Your desired function/property here.]</pre>
</div></div><h1 id="AmplifiAPI-APIIndex">API Index</h1><p>All documentation provided in the table below describes and demonstrates how developers can leverage Amplifi to achieve their game development and audio management goals. </p><p>All internal modules are described in documentation under the <a href="Support-Modules_28672003.html" data-linked-resource-id="28672003" data-linked-resource-version="9" data-linked-resource-type="page">Support Modules</a> section. As these classes are not outward accessible, limited documentation is provided beyond general descriptions of the purpose each module serves.</p><div class="table-wrap"><table data-table-width="760" data-layout="default" data-local-id="18eb3fdb-166d-4465-9bf8-0718b3c96f0f" class="confluenceTable"><colgroup><col style="width: 399.0px;"/><col style="width: 361.0px;"/></colgroup><tbody><tr><th class="confluenceTh"><p><strong>Class</strong></p></th><th class="confluenceTh"><p><strong>Type</strong></p></th></tr><tr><td class="confluenceTd"><p><a href="Amplifi.AmplifiContext_29097985.html" data-linked-resource-id="29097985" data-linked-resource-version="14" data-linked-resource-type="page">AmplifiContext</a></p></td><td class="confluenceTd"><p>Scriptable Object</p></td></tr><tr><td class="confluenceTd"><p><a href="Amplifi.AmplifiControlTower_29130753.html" data-linked-resource-id="29130753" data-linked-resource-version="10" data-linked-resource-type="page">AmplifiControlTower</a></p></td><td class="confluenceTd"><p>Static Class</p></td></tr><tr><td class="confluenceTd"><p><a href="Amplifi.AmplifiEngine_29130763.html" data-linked-resource-id="29130763" data-linked-resource-version="13" data-linked-resource-type="page">AmplifiEngine</a></p></td><td class="confluenceTd"><p>Monobehavior</p></td></tr><tr><td class="confluenceTd"><p><a href="Amplifi.AmplifiMixerSupport_29130773.html" data-linked-resource-id="29130773" data-linked-resource-version="4" data-linked-resource-type="page">AmplifiMixerSupport</a></p></td><td class="confluenceTd"><p>Static Class</p></td></tr></tbody></table></div><p />
                    </div>

                    
                                                      
                </div>             </div> 
            <div id="footer" role="contentinfo">
                <section class="footer-body">
                    <p>Document generated by Confluence on Jun 13, 2024 15:50</p>
                    <div id="footer-logo"><a href="http://www.atlassian.com/">Atlassian</a></div>
                </section>
            </div>
        </div>     </body>
</html>

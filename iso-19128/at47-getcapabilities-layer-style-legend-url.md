# Layer Style Legend URL

**Purpose**: Test that a legend is provided into LegendURL element for each style and supported language defined in the View Service.

**Prerequisites**

**Test method**

* Send one getCapabilities request to the service endpoint for each supported language. Each request has its corresponding language parameter. Into each response:

  * For each [Style](#style) element:

    * Check that zero or one [LegendURL](#legend) element exists. If a legend is provided,
    
        * Check that the node has an 'OnlineResource' child element with a 'xlink:href' attribute.

            * Send a request to the url pointing to the legend.

                * Check that the reponse is a valid image.

* Check manually that the provided legend is in the correct language.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.8 and 4.2.3.3.4.9, Requirement 47

**Test type**: Automated / Manual

**Notes**

The multiplicity of this element 0 or 1 for each style and each supported language.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Style <a name="style"></a> | wms:Capability/\*/wms:Layer/\*/wms:Style
LegendURL <a name="legend"></a> | wms:Capability/*/wms:Layer/wms:Style/wms:LegendURL

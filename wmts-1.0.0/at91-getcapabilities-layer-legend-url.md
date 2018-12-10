# Layer Style Legend URL

**Purpose**: Test that if a legend is provided it is mapped into a LegendURL element and the language is according with the language of the capabilities document.

**Prerequisites**

**Test method**

* Send one getCapabilities request to the service endpoint for each supported language. Each request has its corresponding language parameter. Into each response:

  * For each [Style](#style) element:

    If a [LegendURL](#legend) element is provided:

    * Send a request to the resource into "xlink:href" attribute:

      * Check that the format of the response match with the format defined in the "format" attribute of the [LegendURL](#legend) element.

      * Check manually that the language of the texts included in the legend match with the requested language.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4.9, Requirement 91

**Test type**: Automated/Manual

**Notes**

The multiplicity of this element 0 or more for each style for each supported language.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Style <a name="style"></a> | Contents/Layer/Style
LegendURL <a name="legend"></a> | Contents/Layer/Style/ows:LegendURL
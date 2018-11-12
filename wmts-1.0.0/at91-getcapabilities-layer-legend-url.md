# Layer Style Legend URL

**Purpose**: Test that a legend is provided into LegendURL element for each style and supported language.

**Prerequisites**

**Test method**

* Send one getCapabilities request to the service endpoint for each supported language. Each request has its corresponding language parameter. Into each response:

  * For each wms:Style element:

    * Check if a legend is provided in the [LegendURL](#legend) element.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4.9, Requirement 91

**Test type**: Automated

**Notes**

The multiplicity of this element 1 for each style and each supported language.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
LegendURL <a name="legend"></a> | Contents/Layer/Style/ows:LegendURL
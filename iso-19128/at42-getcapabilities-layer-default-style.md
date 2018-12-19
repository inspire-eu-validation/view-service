# Layer Default Style

**Purpose**: Test that a style is provided with the name of the default style defined in the INSPIRE Data Specification for the theme of the layer.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each named [Layer](#layer) element:

    * If the INSPIRE Data Specification defines a default style for the harmonised layer,

      * Check if the [Style Name](#styleName1) of one of the [Style](#style) elements provided in the layer itself or inherited from a parent layer is equal to the name of the default style defined in the Data Specification.

    * Otherwise, a default style for that harmonised layer name is not defined in the Theme INSPIRE Data Specification, therefore the test passes.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.8, Requirement 42

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 for harmonised layers with default style specified in the Data Specification. The style may be provided in the layer itself or inherited from a parent layer.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | wms:Capability/*/wms:Layer
Style <a name="style"></a> | wms:Capability/*/wms:Layer/wms:Style
Style Name <a name="styleName1"></a> | wms:Capability/*/wms:Layer/wms:Style/wms:Name

# Layer Style Title and Name

**Purpose**: Test that each style has a human-readable name mapped to Title element and a unique identifier mapped to Name element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each [Style](#style) element in each [Layer](#layer) element:

    * Check if exactly one [Title](#title) element exists and it is a non-empty value.

    * Check if exactly one [Style Name](#styleName1) element exists and it is a non-emtpy value.

      * Check if the [Style Name](#styleName1) is unique within the style elements of the layer.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.8, Requirement 46

**Test type**: Automated

**Notes**

The multiplicity of [Title](#title) and [Style Name](#styleName1) is 1 in each style.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | wms:Capability/*/wms:Layer
Style <a name="style"></a> | wms:Capability/*/wms:Layer/wms:Style
Title <a name="title"></a> | wms:Capability/*/wms:Layer/wms:Style/wms:Title
Style Name <a name="styleName1"></a> | wms:Capability/*/wms:Layer/wms:Style/wms:Name

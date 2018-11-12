# Layer Style Title and Name

**Purpose**: Test that each style has a human-readable name mapped to Title element and a unique identifier mapped to Name element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:
  
  * For each wms:Style element:

    * Check if a human-readable name is mapped to the [Title](#title) element.

    * Check if the Unique Identifier is mapped to the [Name](#name) element.

      * Check if the [Name](#name) is unique within the style elements of the layer.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.8, Requirement 46

**Test type**: Automated

**Notes**

The multiplicity of both elements is 1 in each style.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="title"></a> | wms:Capability/wms:Layer/*/wms:Style/wms:Title
Name <a name="name"></a> | wms:Capability/wms:Layer/*/wms:Style/wms:Name
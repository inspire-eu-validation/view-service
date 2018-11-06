# Layer Style

**Purpose**: Test that each style is composed of a Title and a Unique Identifier.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each wms:Style element:

    * Check if it is given a [Title](#title) and a [unique identifier](#identifier).
    * Check if the [unique identifier](#identifier) is unique within the style elements of the layer.

**Reference(s)**
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.8, Requirement 41

**Test type**: Automated

**Notes**

The multiplicity of both elements is 1 in each style.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="title"></a> | wms:Capability/wms:Layer/wms:Style/wms:Title
Identifier <a name="identifier"></a> | wms:Capability/wms:Layer/wms:Style/wms:Name

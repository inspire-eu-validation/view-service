# Layer Category Layer

**Purpose**: Test that if exist a category layer with nested sub-layers it contains a Name element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if exists a [Layer](#layer) element with nested sub-layers. If true,

    * Check that the [Category Layer](#categoryLayer) contains a [Name](#name) element.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.11, Requirement 49

**Test type**: Automated

**Notes**

The multiplicity of the element Name is 1.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a>   | wms:Capability/wms:Layer/wms:Layer
Category Layer <a name="categoryLayer"></a>   | wms:Capability/wms:Layer
Name <a name="name"></a>   | wms:Capability/wms:Layer/wms:Name

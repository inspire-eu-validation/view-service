# LinkViewService Discover

**Purpose**: 

Test that cascaded layers provide a valid metadata through a Discovery Service.

**Prerequisites**

**Test method**

* For every cascaded layer,

    * Check that [Online Resource](#onlineResource) is provided and it has an attribute 'xlink:href' with a non empty value.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 61

**Test type**: Automatic

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Online Resource <a name="onlineResource"></a> | wms:Capability/*/wms:Layer/wms:MetadataURL/wms:OnlineResource
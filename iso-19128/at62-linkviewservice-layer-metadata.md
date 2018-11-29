# LinkViewService Layer Metadata

**Purpose**:

Test that the cascaded layer metadata is included as in the original view service.

**Prerequisites**

**Test method**

* For every cascaded layer,

    * Send an http to request to [Layer Metadata URL](#layerMetadataUrl).

        * Check if the response is a metadata document.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 62

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer Metadata URL<a name="layerMetadataUrl"></a> | wms:Capability/*/wms:Layer/wms:MetadataURL/wms:OnlineResource/@xlink:href
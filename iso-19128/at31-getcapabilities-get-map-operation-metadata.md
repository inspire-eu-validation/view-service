# GetMap Operation Metadata

**Purpose**: Test that the GetMap metadata is mapped to the wms:GetMap element and that either PNG or GIF format (without LZW compression) with transparency is supported.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if there is exactly one [GetMap](#GetMap) node in the [Request](#Request) section of the GetCapabilities response. If it does,

    * Check if the GetMap node contains a [Format](#Format) element with values "image/png" and/or "image/gif".

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.2.2, Requirement 31

**Test type**: Automated

**Notes**

The multiplicity of this element is 1.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Request <a name="Request"></a> | wms:Capability/wms:Request
GetMap <a name="GetMap"></a> | wms:Capability/wms:Request/wms:GetMap
Format <a name="Format"></a> | wms:Capability/wms:Request/wms:GetMap/wms:Format

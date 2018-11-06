# GetCapabilities Operation Metadata

**Purpose**: Test that GetCapabilities operation metadata is mapped to the wms:GetCapabilities element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if a [GetCapabilities](#getCapabilities) element is provided within the wms:Request element.

**Reference(s)**
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.2.1, Requirement 30

**Test type**: Automated

**Notes**

The multiplicity of this element is 1.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
GetCapabilities <a name="getCapabilities"></a> | wms:Capability/wms:Request/wms:GetCapabilities

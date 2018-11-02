# Map Coupled Resource metadata

**Purpose**: Test that...

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * If there is a MetadataURL node for a layer:

    * Check if the linkage 

**Reference(s)**
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.5, Requirement 13

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
MetadataURL <a name="MetadataURL"></a>  |  wms:Capability/wms:Layer/MetadataURL/OnlineResource/@xlink:href
# Map Coupled Resource metadata

**Purpose**: Test that...

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * If there is a MetadataURL node for a layer:

    * In case the linkage to the dataset or series on which the service operates are available,
      * Check if the linkage to these resources is provided into the MetadataURL element as stated by the INSPIRE Metadata Technical Guidance.

**Reference(s)**
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.5, Requirement 13
* [TG MD](./README.md#ref_TG_MD)

**Test type**: Manual

**Notes**

The multiplicity of this element is 1 or more.

It is not possible to test automatically the availability of the of the linkage to the dataset or series on which the service operates.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
MetadataURL <a name="MetadataURL"></a>  |  wms:Capability/*/wms:Layer/MetadataURL/OnlineResource/@xlink:href
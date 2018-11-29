# Map Coupled Resource metadata

**Purpose**: Test that a url is provided if the metadata of a layer exists.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:
  
  * If the metadata for a layer exists,

    * Check that the url is provided in the 'xlink:href' attribute of an [OnlineResource](#onlineResource) element of the layer.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.5, Requirement 13
* [TG MD](./README.md#ref_TG_MD)

**Test type**: Manual

**Notes**

It is not possible to test automatically if the metadata of a layer exists.
It is not possible to test automatically the availability of the linkage to the metadata of layer provided by the service.
It is not possible to test automatically the availability of the linkage to the dataset or series on which the service operates.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
OnlineResource <a name="onlineResource"></a>  |  wms:Capability/wms:Layer/MetadataURL/OnlineResource

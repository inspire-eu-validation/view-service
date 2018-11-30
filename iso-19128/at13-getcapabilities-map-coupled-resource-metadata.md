# Map Coupled Resource metadata

**Purpose**: Test that a url is provided if the metadata of a layer exists.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:
  
  * Check manually if the metadata for a layer exists. If it does,

    * Check manually if the url of the layer's metadata is provided in the 'xlink:href' attribute of an [OnlineResource](#onlineResource) element of the layer.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.5, Requirement 13
* [TG MD](./README.md#ref_TG_MD)

**Test type**: Manual

**Notes**

It is not possible to test automatically when a layer provided by the view service has a metadata file/record in any other service if it is not given explicitly.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
OnlineResource <a name="onlineResource"></a>  |  wms:Capability/wms:Layer/MetadataURL/OnlineResource

# Map Coupled Resource metadata URL

**Purpose**: Test that, in case of a MetadataURL element is provided, a linkage is provided to a metadata document.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:
  
  * If there is a [MetadataURL](#metadataURL) node for a layer:

    * Check if the MetadataURL element is populated with a URL that allows access to unambiguous metadata record. The URL must be encoded into the "xlink:href" attribute of an [OnlineResource](#onlineResource) element.
    
    * One of the following checks must be passed:

      * Check if sending a HTTP/GET request to the GetRecorById of the Discovery Service, a valid response is returned.

      * Check if a direct link is provided to the ISO19139 metadata document.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.5, Requirement 14

**Test type**: Automated

**Notes**

The multiplicity of this element is 0 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
MetadataURL <a name="metadataURL"></a>  |  wms:Capability/*/wms:Layer/MetadataURL
OnlineResource/@xlink:href <a name="onlineResource"></a>  |  wms:Capability/wms:Layer/MetadataURL/OnlineResource/@xlink:href
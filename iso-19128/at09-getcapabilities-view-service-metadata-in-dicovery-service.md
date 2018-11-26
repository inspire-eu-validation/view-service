# View Service Metadata in Discovery Service

**Purpose**: Test that the metadata of the View Service is published in a Discovery Service.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

  * If scenario 1,
  
    * Check that [MetadataUrl](#metadataUrl) exists. Otherwise the test fails.

  * Regardless of the scenario, if [MetadataUrl](#metadataUrl) exists,

    * Send a request to get the metadata document.

        * Check that the metadata document is correct.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1, Requirement 9

**Test type**: Automated

**Notes**

Limitations: The requirement in the technical guidance specify that the View Service Metadata shall be published in an INSPIRE Discovery Service. It is possible to check that a [MetadataUrl](#metadataUrl) is provided in the capabilities document. However, this element is mandatory only in the scenario 1.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
 MetadataUrl <a name="metadataUrl"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataUrl

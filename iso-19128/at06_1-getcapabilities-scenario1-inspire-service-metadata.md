# Scenario 1 - MetadataURL references INSPIRE service metadata

**Purpose**: Test that service metadata is referenced through the MetadataURL element within the ExtendedCapabilities section.

**Prerequisites**

**Test method**

* Send a GetCapabilities request.

  * Check that [MetadataUrl](#metadataUrl) element contains a valid URL:
    * Send a request to get the metadata document.
    * Check that the metadata document obtained is correct.

  * Regardless of the scenario, if [MetadataUrl](#metadataUrl) exists,

    * Send a request to get the metadata document.
    * Check that the metadata document obtained is correct.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1, Requirement 6 - Section 1

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
MetadataUrl <a name="metadataUrl"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataUrl

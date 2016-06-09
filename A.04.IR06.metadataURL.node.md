# A.04.IR06.metadataURL.node

**Purpose**: The element within the extended INSPIRE capabilities of an ISO 19128 – WMS 1.3.0 wms:Capability element shall be used to reference the INSPIRE service metadata available through an INSPIRE Discovery Service. 

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* First check if the metadataURL node exists in the ExtendedCapabilities section. If yes:
  * Resolve the URL.
  * Verify that the response is an XML document with a root element csw:GetRecordByIdResponse or gmd:MD_Metadata.
  * In case of a csw:GetRecordByIdResponse document, use the first gmd:MD_Metadata child element. Issue an error if there is no such element.
  * Validate the gmd:MD_Metadata element against the [ISO metadata schema](http://www.isotc211.org/2005/gmd/gmd.xsd). Report errors.
* If no metadata URL is given then all mandatory [ISO 19128 metadata elements](see [TG VS](README.md#ref_TG_VS), Table 3) must exist in the ExtendedCapabilities section.

**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1
* IR Annex III, Part A, Chapter 2.2.1

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
metadataURL <a name="metadataURL"></a>   | /WMS_Capability/Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataUrl
ExtendedCapabilities <a name="ExtendedCapabilities"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities

# MetadataURL reference INSPIRE service metadata

**Purpose**: The `<inspire_common:MetadataURL>` element within the extended INSPIRE capabilities of an ISO 19128 – WMS 1.3.0 `wms:Capability` element shall be used to reference the INSPIRE service metadata available through an INSPIRE Discovery Service. 

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)

**Test method**

* First check if the service uses [scenario 2](#scenario-2) for the metadata. If not the [metadataURL](#metadataURL) node must exist in the [ExtendedCapabilities](#ExtendedCapabilities) section, otherwise the test fails.
* If the [metadataURL](#metadataURL) node exists in the [ExtendedCapabilities](#ExtendedCapabilities) section:
  * Verify that the response to a HTTP GET request of the [metadataURL](#metadataURL) is an XML document with a root element csw:GetRecordByIdResponse or gmd:MD_Metadata.
  * In case of a csw:GetRecordByIdResponse document, use the first gmd:MD_Metadata child element. Issue an error if there is no such element.
  * Validate the gmd:MD_Metadata element against the [ISO metadata schema](http://www.isotc211.org/2005/gmd/gmd.xsd). Report errors.

**Reference(s)**:

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), Chapter 4.2.3.3.1

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
metadataURL <a name="metadataURL"></a>   | /wms:WMS_Capability/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataUrl
ExtendedCapabilities <a name="ExtendedCapabilities"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities
scenario 2 <a name="scenario-2"/> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities[inspire_common:ResourceLocator or inspire_common:ResourceType or inspire_common:TemporalReference or inspire_common:Conformity or inspire_common:MetadataPointOfContact or inspire_common:MetadataDate or inspire_common:SpatialDataServiceType or inspire_common:MandatoryKeyword or inspire_common:Keyword]

# Point of contact details

**Purpose**: INSPIRE is more demanding than ISO 19115 by mandating both the name of the organisation, and a contact e-mail address. The role of the responsible party serving as a metadata point of contact is out of scope of the Metadata Regulation INS MD,
but this property is mandated by ISO 19115. Its value shall be defaulted to 'OptionOfContact'.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)
* [Extended Capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/extended-capabilities)

**Test method**

This test only applies to [scenario 2](#scenario-2). Otherwise the test case is skipped.

* Check if there is a [MetadataPointOfContact](#MetadataPointOfContact) node in the ExtendedCapabilities section.  If yes:
  * Check if there is a [OrganisationName](#OrganisationName) node and a EmailAddress node in the MetadataPointOfContact section.

**Reference(s)**:
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), Chapter 4.2.3.3.1.15, Requirements 27, 28


**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
MetadataPointOfContact <a name="MetadataPointOfContact"></a> | ./Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataPointOfContact
OrganisationName <a name="OrganisationName"></a> | ./wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataPointOfContact/inspire_common:OrganisationName
EmailAddress <a name="EmailAddress"></a> | ./wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataPointOfContact/inspire_common:EmailAddress
Scenario 2 <a name="scenario-2"/> | ./wms:Capability/inspire_vs:ExtendedCapabilities[inspire_common:ResourceLocator or 
inspire_common:ResourceType or inspire_common:TemporalReference or inspire_common:Conformity or inspire_common:MetadataPointOfContact or 
inspire_common:MetadataDate or inspire_common:SpatialDataServiceType or inspire_common:MandatoryKeyword or inspire_common:Keyword]

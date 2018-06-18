# Date type

**Purpose**: To be compliant with the INSPIRE Metadata Regulation INS MD and with ISO 19115 one of following dates shall be used: date of publication, date of last revision, or the date of creation. Date of last revision is preferred. The date shall be expressed in conformity with the INS MD.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)

**Test method**

This test only applies to [scenario 2](#scenario-2). Otherwise the test case is skipped.

Check, if there is either a DateOfCreation node, a DateOfPublication node or a DateOfLastRevision node in the TemporalReference section.

**Reference(s)**:

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), Chapter 4.2.3.3.1.9

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
scenario 2 <a name="scenario-2"/> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities[inspire_common:ResourceLocator or inspire_common:ResourceType or inspire_common:TemporalReference or inspire_common:Conformity or inspire_common:MetadataPointOfContact or inspire_common:MetadataDate or inspire_common:SpatialDataServiceType or inspire_common:MandatoryKeyword or inspire_common:Keyword]
DateOfCreation <a name="DateOfCreation"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference/inspire_common:DateOfCreation
DateOfPublication <a name="DateOfPublication"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference/inspire_common:DateOfPublication
DateOfLastRevision <a name="DateOfLastRevision"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference/inspire_common:DateOfLastRevision
TemporalReference <a name="TemporalReference"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference

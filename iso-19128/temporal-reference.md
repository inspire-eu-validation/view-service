# Temporal reference

**Purpose**: As the Temporal Reference is not directly supported by ISO 19128 – WMS 1.3.0 an extension shall be used to map this to an element within an element.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)
* [Extended Capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/extended-capabilities)

**Test method**

This test only applies to [scenario 2](#scenario-2). Otherwise the test case is skipped.

Check that if a [TemporalExtent](#TemporalExtent) element exists, that it is contained within the [TemporalReference](#TemporalReference) node of the ExtendedCapabilities section.


**Reference(s)**:
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), Chapter 4.2.3.3.1.9, Requirement 21

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Scenario 2 <a name="scenario-2"/> | ./wms:Capability/inspire_vs:ExtendedCapabilities[inspire_common:ResourceLocator or 
inspire_common:ResourceType or inspire_common:TemporalReference or inspire_common:Conformity or inspire_common:MetadataPointOfContact or 
inspire_common:MetadataDate or inspire_common:SpatialDataServiceType or inspire_common:MandatoryKeyword or inspire_common:Keyword]
TemporalReference <a name="TemporalReference"></a> | ./wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference
TemporalExtent <a name="TemporalExtent"></a> | ./wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference/inspire_common:TemporalExtent


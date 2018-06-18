# Keyword node

**Purpose**: The keywords shall be mapped to the capabilities extension and within an element.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)
* [Extended Capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/extended-capabilities)

**Test method**

This test only applies to [scenario 2](#scenario-2). Otherwise the test case is skipped.

* Check if there are a [Keyword](#Keyword) node and a [MandatoryKeyword](#MandatoryKeyword) node in the ExtendedCapabilities section
* Check that there exists at least one keyword element containing one of the keywords listed in COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008, Part D, 4.Classification of Spatial data Services (the lowerCamelCase terms in parenthesis).

**Reference(s)**:
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), Chapter 4.2.3.3.1.7, Requirement 16, 18

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Keyword <a name="Keyword"></a> | ./wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:Keyword
MandatoryKeyword <a name="MandatoryKeyword"></a> | ./wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MandatoryKeyword
scenario 2 <a name="scenario-2"/> | ./wms:Capability/inspire_vs:ExtendedCapabilities[inspire_common:ResourceLocator or inspire_common:ResourceType or inspire_common:TemporalReference or inspire_common:Conformity or inspire_common:MetadataPointOfContact or inspire_common:MetadataDate or inspire_common:SpatialDataServiceType or inspire_common:MandatoryKeyword or inspire_common:Keyword]

# Map SDS Type with ExtendedCapabilities

**Purpose**: For the Spatial Data Service Type as defined by the INSPIRE Metadata Regulation INS MD ('view') an extension shall 
be used to map this to an element within an element. For an INSPIRE View Service the Spatial Data Service Type shall have a fixed value 'view' according to INSPIRE Metadata Regulation INS MD Part 3.

**Prerequisites**

* [Schema validation](./schema-validation)
* [Extended Capabilities](./extended-capabilities)

**Test method**

This test only applies to [scenario 2](#scenario-2). Otherwise the test case is skipped.

* Check if there is a SpatialDataServiceType node in the ExtendedCapabilities section. If yes, check that it is set to 'view'.

**Reference(s)**: 
* [TG VS](./README#ref_TG_VS), Chapter 4.2.3.3.1.6, Requirement 15

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
SpatialDataServiceType <a name="SpatialDataServiceType"></a>   | ./Capability/inspire_vs:ExtendedCapabilities/inspire_common:SpatialDataServiceType
Scenario 2 <a name="scenario-2"></a> | ./wms:Capability/inspire_vs:ExtendedCapabilities[inspire_common:ResourceLocator or 
inspire_common:ResourceType or inspire_common:TemporalReference or inspire_common:Conformity or inspire_common:MetadataPointOfContact or 
inspire_common:MetadataDate or inspire_common:SpatialDataServiceType or inspire_common:MandatoryKeyword or inspire_common:Keyword]

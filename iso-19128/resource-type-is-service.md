# Resource type is Service

**Purpose**: Within the scope defined by the INSPIRE directive the value of the Resource Type shall be fixed to service for spatial data services. As the Resource Type is not supported by ISO 19128 – WMS 1.3.0, an extension shall be used to map this to an element within an element.

**Prerequisites**

* [Schema validation](./schema-validation)
* [Extended Capabilities](./extended-capabilities)


**Test method**

This test only applies to [scenario 2](#scenario-2). Otherwise the test case is skipped.

* Check if there is a [ResourceType](#ResourceType) node in the ExtendedCapabilities section.
* If yes check that it is set to 'service'.

**Reference(s)**:
* [TG VS](./README#ref_TG_VS), Chapter  4.2.3.3.1.3, Requirement 11 

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
ResourceType <a name="ResourceType"></a>   | ./wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:ResourceType
Scenario 2 <a name="scenario-2"></a> | ./wms:Capability/inspire_vs:ExtendedCapabilities[inspire_common:ResourceLocator or inspire_common:ResourceType or inspire_common:TemporalReference or inspire_common:Conformity or inspire_common:MetadataPointOfContact or 
inspire_common:MetadataDate or inspire_common:SpatialDataServiceType or inspire_common:MandatoryKeyword or inspire_common:Keyword]

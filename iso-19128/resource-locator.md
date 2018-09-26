# Resource Locator

**Purpose**: An extension shall be used to map Resource Locator to an element within an element.

**Prerequisites**

* [Schema validation](./schema-validation)
* [Extended Capabilities](./extended-capabilities)

**Test method**

This test only applies to [scenario 2](#scenario-2). Otherwise the test case is skipped.

Check if there is a [ResourceLocator](#ResourceLocator) node in the ExtendedCapabilities section.

**Reference(s)**:
* [TG VS](./README#ref_TG_VS), Chapter 4.2.3.3.1.4, Requirement 12

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
ResourceLocator <a name="ResourceLocator"></a>   | ./wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:Conformity/inspire_common:Specification/inspire_common:ResourceLocator/inspire_common:URL
Scenario 2 <a name="scenario-2"/> | ./wms:Capability/inspire_vs:ExtendedCapabilities[inspire_common:ResourceLocator or 
inspire_common:ResourceType or inspire_common:TemporalReference or inspire_common:Conformity or inspire_common:MetadataPointOfContact or 
inspire_common:MetadataDate or inspire_common:SpatialDataServiceType or inspire_common:MandatoryKeyword or inspire_common:Keyword]

# Map SDS Type with Extended Capabilities

**Purpose**: Test that a SpatialDataService Type element is given within the ExtendedCapabilities section.

**Prerequisites**

**Test method**

This test only applies to [scenario 2](./README.md#scenarios). Otherwise the test case is skipped.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if there is a [SpatialDataServiceType](#SpatialDataServiceType) element into the ExtendedCapabilities section.

  * Check that the [SpatialDataServiceType](#SpatialDataServiceType) element has a fixed value equal to 'view' as defined in [INS MD Part 3].

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.6, Requirement 15
* [INS MD](./README.md#ref_INS_MD), Part 3

**Test type**: Automated

**Notes**

The multiplicity of this element is 1.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
SpatialDataServiceType <a name="SpatialDataServiceType"></a>   | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:SpatialDataServiceType
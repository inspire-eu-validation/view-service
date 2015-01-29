# A.15.IR15.spatialdataservicetype.node

**Purpose**: For the Spatial Data Service Type as defined by the INSPIRE Metadata Regulation INS MD (‘view’) an extension shall be used to map this to an element within an element. For an INSPIRE View Service the Spatial Data Service Type shall have a fixed value “view” according to INSPIRE Metadata Regulation INS MD Part 3.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* Check if there is a SpatialDataServiceType node in the ExtendedCapabilities section
* If yes, check that it is set to 'view'.


**Reference(s)**: 
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.6

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
SpatialDataServiceType <a name="SpatialDataServiceType"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:SpatialDataServiceType
ExtendedCapabilities <a name="ExtendedCapabilities"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities

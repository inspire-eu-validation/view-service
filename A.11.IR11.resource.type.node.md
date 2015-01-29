# A.11.IR11.resource.type.node

**Purpose**: Within the scope defined by the INSPIRE directive the value of the Resource Type shall be fixed to service for spatial data services. As the Resource Type is not supported by ISO 19128 – WMS 1.3.0, an extension shall be used to map this to an element within an element.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* First check if there is a ResourceType node in the ExtendedCapabilities section
* If yes, check that it is set to 'service'.

**Reference(s)**: 
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.3

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ResourceType <a name="ResourceType"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:ResourceType
ExtendedCapabilities <a name="ExtendedCapabilities"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities

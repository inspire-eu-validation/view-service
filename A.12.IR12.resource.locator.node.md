# A.12.IR12.resource.locator.node

**Purpose**: An extension shall be used to map Resource Locator to an element within an element.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* Check if there is a ResourceLocator node in the ExtendedCapabilities section.


**Reference(s)**: 
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.4

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ResourceLocator <a name="ResourceLocator"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:Conformity/inspire_common:Specification/inspire_common:ResourceLocator/inspire_common:URL
ExtendedCapabilities <a name="ExtendedCapabilities"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities

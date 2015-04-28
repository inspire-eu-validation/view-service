# A.10.IR10.metadata.elements

**Purpose**: An INSPIRE View service shall contain the INSPIRE metadata elements set out in the Metadata Regulation INS MD as shown in Table 3.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* Check if all mandataory ISO 19128 metadata elements[1] exist in the ExtendedCapabilities section.

[1] [TG VS](README.md#ref_TG_VS), Table 3

**Reference(s)**: 
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="ExtendedCapabilities"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities

# Check Conformity node

**Purpose**: An extension shall be used to map this to an `<inspire_common:Conformity>` element within an ` <inspire_vs:ExtendedCapabilities>` element.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.
* No metadata URL is given in test case [MetadataURL reference INSPIRE service metadata](MetadataURL reference INSPIRE service metadata.md)

**Test method**

* Check if there is a Conformity node in the ExtendedCapabilities section.

**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.11

**Test type:** Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Conformity <a name="Conformity"></a> | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:Conformity
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities

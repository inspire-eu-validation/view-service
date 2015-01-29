# A.22.IR22.conformity.deegree.node

**Purpose**: The INSPIRE Metadata Regulation INS MD requires that metadata shall include information on the degree of conformity with the implementing rules provided in Art. 7.1 (Interoperability of spatial data sets and services) of the INSPIRE Directive Directive 2007/2/EC.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* Check if there is a Conformity node in the ExtendedCapabilities section.
* If yes, check that it has a Deegree node with one of these values: notEvaluated, conformant, notConformant.


**Reference(s)**: 
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.11

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Conformity <a name="Conformity"></a> | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:Conformity
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities
Degree <a name="Degree"></a> | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:Conformity/inspire_common:Degree

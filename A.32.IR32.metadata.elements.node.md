# A.32.IR32.metadata.elements.node

**Purpose**: The description of a layer shall use elements defined for the service capabilities in the ISO 19128 standard. This description shall specify the role of some parameters for the INSPIRE View Service as stated in the Regulation on INSPIRE Network Services INS NS.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* Then check if all mandatory metadata elements* exist in each Layer section.

**Reference(s)**: 
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.4
* IR Annex III, Part A, Chapter 2.2.4

**Notes**

* * see INS VS, Table 4
* see also Requirements 33 - 49

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="Layer"></a>   | /WMS_Capabilities/Capability/Layer



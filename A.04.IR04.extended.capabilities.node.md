# A.04.IR04.extended.capabilities.node

**Purpose**: The metadata response parameters shall be provided through the service Capabilities, as defined in the WMS Standard ISO 19128, Section 7.2.4. These capabilities are mandatory and defined when a WMS is set up. They consist of service information, supported operations and parameters values. The extended capabilities section shall be used to fully comply with the INSPIRE View Service metadata requirements (see section 4.2.3.3.1).

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* First check if the service document contains the ExtendedCapabilities node.
* Then check that the extended capabilities element validates against the INSPIRE schemas.

**Reference (s)**: [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.1

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="extendedCapabilities"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities

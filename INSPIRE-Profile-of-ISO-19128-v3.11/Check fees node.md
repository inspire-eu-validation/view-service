# Check fees node

**Purpose**: Metadata concerning to conditions for access and use shall be mapped to the wms:Fees element of the capabilities. If no conditions apply to the access and use of the resource, "no conditions apply" shall be used. If conditions are unknown "conditions unknown" shall be used.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* Check if there is a Fees node in the Service Capabilities
* If yes, check that it has one of the values: no conditions apply, conditions unknown or free text.

**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.12

**Test type:** Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Fees <a name="Fees"></a> | /WMS_Capabilities/Service/Fees
Service <a name="Service"></a> | /WMS_Capabilities/Service

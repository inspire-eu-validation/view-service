# Fees node

**Purpose**: Test that a Fees node is provided defining the conditions for access and use.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if is provided at least one [Fees](#Fees) node defining the conditions for access and use. 

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.12, Requirement 24

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

If no conditions apply to the access and use of the resource, "no conditions apply" shall be used. If conditions are unknown "conditions unknown" shall be used.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Fees <a name="Fees"></a> | wms:Service/wms:Fees
Capabilities
# Fees node

**Purpose**: Metadata concerning to conditions for access and use shall be mapped to the wms:Fees element of the capabilities. If no conditions apply to the access and use of the resource, "no conditions apply" shall be used. If conditions are unknown "conditions unknown" shall be used.

**Prerequisites**

* [Schema validation](./schema-validation)
* [Extended Capabilities](./extended-capabilities)

**Test method**

This test only applies to [scenario 2](#scenario-2). Otherwise the test case is skipped.
* Check if there is a Fees node in the Service Capabilities
* If yes, check that it has one of the values: "no conditions apply" or "conditions unknown".

**Reference(s)**:
* [TG VS](./README#ref_TG_VS), Chapter 4.2.3.3.1.12, Requirement 24

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Fees <a name="Fees"></a> | ./wms:Service/wms:Fees

Capabilities
# Fees node

**Purpose**: Metadata concerning to conditions for access and use shall be mapped to the wms:Fees element of the capabilities. If no conditions apply to the access and use of the resource, "no conditions apply" shall be used. If conditions are unknown "conditions unknown" shall be used.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)
* [Extended Capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/extended-capabilities)

**Test method**

This test only applies to [scenario 2](#scenario-2). Otherwise the test case is skipped.
* Check if there is a Fees node in the Service Capabilities
* If yes, check that it has one of the values: "no conditions apply" or "conditions unknown".

**Reference(s)**:
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), Chapter 4.2.3.3.1.12, Requirement 24

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Fees <a name="Fees"></a> | ./wms:Service/wms:Fees

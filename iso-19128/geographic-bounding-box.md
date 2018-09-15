#  EX_GeographicBoundingBox

**Purpose**: Geographic Bounding Box shall be mapped to the EX_GeographicBoundingBox element of Layer elements.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)
* [Extended Capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/extended-capabilities)

**Test method**

This test only applies to [scenario 2](#scenario-2). Otherwise the test case is skipped.
* Check if there is a EX_GeographicBoundingBox node in each Layer section of the Capabilities section.

**Reference(s)**:

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), Chapter 4.2.3.3.1.8, Requirement 19

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
EX_GeographicBoundingBox <a name="EX_GeographicBoundingBox"></a> | ./wms:Capability/wms:Layer/wms:EX_GeographicBoundingBox


# ETRS89 or ITRS coordinate reference system

**Purpose**: All INSPIRE spatial datasets must be provided at using at least one geographical coordinate system based on either ETRS89 (for datasets within continental Europe) or ITRS (outside continental Europe).

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)

**Test method**

For each [Layer](#layer):
* Check if the text content of at least one of the [CRS elements](#crs) matches the CRS identifier of one of the ETRS89 based or ITRS based coordinate systems.
* If no match is found, repeat the same test recursively with the [Parent layer](#parent_layer), if one exists, until a match is found or no parent layer is found.
* If CRS match is found, pass the test, otherwise fail the test.


**Reference(s)**:

 * [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), chapter 4.2.3.3.4.7 Coordinate reference systems

**Test type**: Automated

**Notes**

This test is a tricky one and will not be complete without a machine-readable "whitelist" register of the acceptable CRSes with their CRS identifiers and commonly used aliases ("label" and "URL" versions). To implement the test this kind on publicly available, official list must be established.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | /wms:WMS_Capabilities/wms:Capability//wms:Layer
CRS elements <a name="crs"></a> | ./wms:CRS
Parent Layer <a name="parent_layer"></a> | ../../wms:Layer

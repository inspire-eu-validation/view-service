#  EX_GeographicBoundingBox

**Purpose**: Geographic Bounding Box shall be mapped to the EX_GeographicBoundingBox element of Layer elements.

**Prerequisites**

* [Schema validation](./schema-validation)

**Test method**

This test only applies to [scenario 2](#scenario-2). Otherwise the test case is skipped.
* Check if there is a [EX_GeographicBoundingBox](#EX_GeographicBoundingBox) node in each Layer section of the Capabilities section.
* Check if the EX_GeographicBoundingBox element is defined by the sub-elements: [westBoundLongitude](#westBoundLongitude), [eastBoundLongitude](#eastBoundLongitude), [southBoundLatitude](#southBoundLatitude) and [northBoundLatitude](#northBoundLatitude)

**Reference(s)**:

* [TG VS](./README#ref_TG_VS), Chapter 4.2.3.3.1.8, Requirement 19

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
EX_GeographicBoundingBox <a name="EX_GeographicBoundingBox"></a> | ./wms:Capability/wms:Layer/wms:EX_GeographicBoundingBox
westBoundLongitude <a name="westBoundLongitude"></a> | ./wms:Capability/wms:Layer/wms:EX_GeographicBoundingBox/wms:westBoundLongitude
eastBoundLongitude <a name="eastBoundLongitude"></a> | ./wms:Capability/wms:Layer/wms:EX_GeographicBoundingBox/wms:eastBoundLongitude
southBoundLatitude <a name="southBoundLatitude"></a> | ./wms:Capability/wms:Layer/wms:EX_GeographicBoundingBox/wms:southBoundLatitude
northBoundLatitude <a name="northBoundLatitude"></a> | ./wms:Capability/wms:Layer/wms:EX_GeographicBoundingBox/wms:northBoundLatitude

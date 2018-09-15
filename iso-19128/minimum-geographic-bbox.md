# Minimum geographic bbox

**Purpose**: This Layer metadata element shall be mapped to the corresponding element.
The minimum bounding rectangle of the area covered by the Layer in all supported CRS shall be given to the extent this is supported by the view service.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/schema-validation)

**Test method**

For each Layer element provided the bounding box for every CRS must be provided.
For each [CRS](#wmsCRS) that is listed for the Layer, check that there is a [BoundingBox](#BoundingBox) node in 
the same Layer section with a corresponding attribute [@CRS](#CRS).

**Reference(s)**:


* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/README#ref_TG_VS), Chapter 4.2.3.3.4.4, Requirement 36

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
CRS <a name="wmsCRS"></a> | ./wms:Capability/wms:Layer/wms:CRS
BoundingBox <a name="BoundingBox"></a> | ./wms:Capability/wms:Layer/BoundingBox
@CRS <a name="CRS"></a> | ./wms:Capability/wms:Layer/BoundingBox[@CRS]

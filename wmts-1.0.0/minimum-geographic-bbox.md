# Minimum geographic bbox

**Purpose**: This Layer metadata element shall be mapped to the corresponding element. The minimum bounding rectangle of the area covered by the Layer in all supported CRS shall be given to the extent this is supported by the view service.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/schema-validation)

**Test method**

For each [Layer element](#layer) provided by the service according to it's Service Metadata:

* In case of a WMTS, the bounding box in an INSPIRE view service is always in WGS84, independent of the supported CRSs. Check that there is one [WGS84BoundingBox element](#wgs84bbox), and that both the [LowerCorner](#lowerCorner) and the [UpperCorner](#upperCorner) elements are given and have two numeric values. The first value, longitude, must be between -180 and 180. The second, latitude, must be between -90 and 90, the upperCorner value must be larger than the lowerCorner value.
* In case of a WMS, the bounding box for every CRS must be provided. For each [CRS](#wmsCRS) that is listed for the [Layer](#Layer), check that there is a [BoundingBox](#BoundingBox) node in the same [Layer](#Layer) section with a corresponding attribute [@CRS](#CRS).

**Reference(s)**:


* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/README#ref_TG_VS) 5.2.3.3.4.4, Requirement 88

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/README#namespaces).

Abbreviation                                               |  XPath expression (relative to Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
CRS <a name="wmsCRS"></a> | ./wmts:Contents/wmts:Layer/wms:CRS
BoundingBox <a name="BoundingBox"></a> | ./wmts:Contents/wmts:Layer/BoundingBox
@CRS <a name="CRS"></a> | ./wmts:Contents/wmts:Layer/BoundingBox[@CRS]

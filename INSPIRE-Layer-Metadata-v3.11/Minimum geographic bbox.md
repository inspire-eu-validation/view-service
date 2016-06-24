# Minimum geographic bbox

**Purpose**: This Layer metadata element shall be mapped to the corresponding element. The minimum bounding rectangle of the area covered by the Layer in all supported CRS shall be given to the extent this is supported by the view service.

**Prerequisites**

* [Validate Schema](Validate Schema.md)

**Test method**

For each [Layer element](#layer) provided by the service according to it's Service Metadata:

* In case of a WMTS, the bounding box in an INSPIRE view service is always in WGS84, independent of the supported CRSs. Check that there is one [WGS84BoundingBox element](#wgs84bbox), and that both the [LowerCorner](#lowerCorner) and the [UpperCorner](#upperCorner) elements are given and have two numeric values. The first value, longitude, must be between -180 and 180. The second, latitude, must be between -90 and 90, the upperCorner value must be larger than the lowerCorner value.
* In case of a WMS, the bounding box for every CRS must be provided. For each [CRS](#wmsCRS) that is listed for the [Layer](#Layer), check that there is a [BoundingBox](#BoundingBox) node in the same [Layer](#Layer) section with a corresponding attribute [@CRS](#CRS).

**Reference(s)**:


* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.4.4
* [TG VS](README.md#ref_TG_VS), chapter 5.2.3.3.4.4

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
Layer <a name="Layer"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer | ISO 19128
                           | /wmts:Capabilities/wmts:Contents/wmts:Layer | WMTS 1.0.0
CRS <a name="wmsCRS"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:CRS | ISO 19128
BoundingBox <a name="BoundingBox"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/BoundingBox | ISO 19128
@CRS <a name="CRS"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/BoundingBox[@CRS] | ISO 19128
WGS84BoundingBox <a name="wgs84bbox"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:WGS84BoundingBox | WMTS 1.0.0
LowerCorner <a name="lowerCorner"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:WGS84BoundingBox/ows:LowerCorner | WMTS 1.0.0
UpperCorner <a name="upperCorner"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:WGS84BoundingBox/ows:UpperCorner | WMTS 1.0.0

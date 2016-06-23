# A.08.IR88.layer.bbox

**Purpose**: Geographic Bounding Box element is used to facilitate geographic searches.

**Prerequisites**

* Test for the schema validity of the ServiceMetadata document has been passed.

**Test method**

For each [Layer element](#layer) provided by the service according to it's Service Metadata:

* Check that there is at least one [WGS84BoundingBox element](#wgs84bbox), and that it both the [LowerCorner](#lowerCorner) and the [UpperCorner](#upperCorner) elements are given and have two values, longitude and latitude, in this order. Usually the coordinates are decimal numbers. For details, see Notes.

**Reference(s)**: [TG VS](README.md#ref_TG_VS), chapter 5.2.3.3.4.4

**Test type**: Automated

**Notes**

Quoting OWS Common 1.1 schema file for PositionType2D:

> Two-dimensional position instances hold the longitude and latitude coordinates of a position in the 2D WGS 84 coordinate reference system. The longitude value shall be listed first, followed by the latitude value, both in decimal degrees. Latitude values shall range from -90 to +90 degrees, and longitude values shall normally range from -180 to +180 degrees. For the longitude axis, special conditions apply when the bounding box is continuous across the +/- 180 degrees meridian longitude value discontinuity:

> a)  If the bounding box is continuous clear around the Earth, then longitude values of minus and plus infinity shall be used.

> b)  If the bounding box is continuous across the value discontinuity but is not continuous clear around the Earth, then some non-normal value can be used if specified for a specific OWS use of the WGS84BoundingBoxType. For more information, see Subclauses 10.4.5 and C.13.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer
WGS84BoundingBox <a name="wgs84bbox"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:WGS84BoundingBox
LowerCorner <a name="lowerCorner"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:WGS84BoundingBox/ows:LowerCorner
UpperCorner <a name="upperCorner"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:WGS84BoundingBox/ows:UpperCorner

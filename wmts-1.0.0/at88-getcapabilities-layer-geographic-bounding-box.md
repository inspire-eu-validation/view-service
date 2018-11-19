# Layer Geographic Bounding Box

**Purpose**: Test that a WGS84BoundingBox element is provided defining the minimum  rectagle bounding the service data.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each Layer element:

    * Check that a [WGS84BoundingBox](#boundingBox) element is given.
    * Check that it is composed by a [LowerCorner](#lowerCorner) and a [UpperCorner](#upperCorner).
        * Check that each element contains a pair of coordinates in decimal degrees. Two numeric values, the first between -180 and 180, and the second between -90 and 90.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4.4, Requirement 88

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 for each layer.

The minimum bounding rectangle in decimal degrees of the area covered by the Layer shall be supplied regardless of what CRS the tileMatrixSet may define and shall use WGS:84 as Coordinate Reference System.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
WGS84BoundingBox <a name="boundingBox"></a> | Contents/Layer/ows:WGS84BoundingBox
Lower corner <a name="lowerCorner"></a> | Contents/Layer/ows:WGS84BoundingBox/ows:LowerCorner
Upper corner <a name="upperCorner"></a> | Contents/Layer/ows:WGS84BoundingBox/ows:UpperCorner
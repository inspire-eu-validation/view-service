# A.11.IR89.etrs89.itrs.crs

**Purpose**: All INSPIRE spatial datasets must be provided at using at least one geographical coordinate system based on either ETRS89 (for datasets within continental Europe) or ITRS (outside continental Europe).

**Prerequisites**

* [A.03.IR05.schema.validation](A.03.IR05.schema.validation.md)

**Test method**

For each [layer](#layer):
* Check if the [TileMatrixSetLink](#TileMatrixSetLink) is the identifier of an [TileMatrixSet](#TileMatrixSet)
* If yes, check that the [TileMatrixSet](#TileMatrixSet) has either no [SupportedCRS element](#crs) or one that matches the CRS identifier of one of the ETRS89 based or ITRS based coordinate systems.
* If CRS match is found, pass the test, otherwise fail the test.


**Reference(s)**:

 * [TG VS](README.md#ref_TG_VS), chapter 5.2.3.3.4.7 Coordinate reference systems

**Test type**: Automated

**Notes**

This test is a tricky one and will not be complete without a machine-readable "whitelist" register of the acceptable CRSes with their CRS identifiers and commonly used aliases ("label" and "URL" versions). To implement the test this kind on publicly available, official list must be established.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer
TileMatrixSetLink <a name="TileMatrixSetLink"/> | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:TileMatrixSetLink/wmts:TileMatrixSet
TileMatrixSet <a name="TileMatrixSet"/> | /wmts:Capabilities/wmts:Contents/wmts:TileMatrixSet/ows:Identifier
SupportedCRS element <a name="crs"></a> | /wmts:Capabilities/wmts:Contents/wmts:TileMatrixSet/ows:SupportedCRS
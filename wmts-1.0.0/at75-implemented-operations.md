# Implemented Operations

**Purpose**: Test that GetCapabilities operation and GetTile operation are implemented.

**Prerequisites**

**Test method**

* Send a GetCapabilities request with mandatory default parameters.
  * Parameters:
    * SERVICE=WMTS
    * REQUEST=GetCapabilities

  * Check that a valid non-empty response is provided.

* Send a GetTile request with mandatory default parameters.
  * Parameters:
    * SERVICE=WMTS
    * REQUEST=GetTile
    * VERSION=1.0.0
    * LAYER
    * STYLE
    * FORMAT
    * TILEMATRIXSET
    * TILEMATRIX
    * TILECOL
    * TILEROW

    (The non-fixed values are taken from the capabilities document)

  * Check that a valid non-empty response is provided. 


**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2, Requirement 75

**Test type**: Automated/Manual

**Notes**

GetTile request has been automated only in the cases when the InspireCRS84Quad TileMatrixSet is implemented. The use of this TileMatrixSet is an INSPIRE Technical Guide recommendation. If this TileMatrixset is not implemented, the GetTile request implementation needs to be tested manually.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------

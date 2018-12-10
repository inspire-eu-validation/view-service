# Common Request Parameters

**Purpose**: Test that common request parameters are implemented for the View Service operations.

**Prerequisites**

**Test method**

* The common request parameters for the View Service operations are:
  * SERVICE
  * REQUEST
  * LANGUAGE

* Check that GetCapabilities operation implements the common request parameters.

* Check that GetTile operation implements the common request parameters.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.1, Requirement 77

**Test type**: Automated/Manual

**Notes**

GetTile request has been automated only in the cases when the InspireCRS84Quad TileMatrixSet is implemented. The use of this TileMatrixSet is an INSPIRE Technical Guide recommendation. If this TileMatrixset is not implemented, the GetTile request common parameters implementation needs to be tested manually.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
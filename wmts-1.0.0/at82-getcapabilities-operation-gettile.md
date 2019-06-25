# Operation GetTile

**Purpose**: Test that a element is provided to map the GetTile operation.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

    * Check that a [Operation](#operation) element is provided with a "name" attribute with a fix value equals to "GetTile".

    For each [Layer](#layer) element in the GetCapabilities document:

    * Check that at least one [Format](#format) element is provided with one of the following values:
      * "image/png"
      * "image/gif"

    * Send a GetTile request for the layer using either "image/png" or "image/gif" format according to the format values defined in the capabilities document for that layer. If both formats are listed in the layer metadata, two seperate requests are made.

      * Check that the returned image is encoded in the requested format.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.2.2, Requirement 82

**Test type**: Automated/Manual

**Notes**

The multiplicity of Operation element is 1 for this purpose.

GetTile request has been automated only in the cases when the InspireCRS84Quad TileMatrixSet is implemented. The use of this TileMatrixSet is an INSPIRE Technical Guide recommendation. If this TileMatrixset is not implemented, the GetTile request response format needs to be tested manually.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Operation <a name="operation"></a> | ows:OperationsMetadata/ows:Operation
Layer <a name="layer"></a> | Contents/Layer
Format <a name="format"></a> | Contents/Layer/Format
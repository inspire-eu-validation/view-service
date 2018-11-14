# ETRS89 or ITRS coordinate reference system

**Purpose**: Test that in case a SupportedCRS element is provide for the TileMatrixSet, the CRS is based on ETRS89 in continental Europe and ITRS outside continental Europe.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each Layer element:

    * Check if the [TileMatrixSetLink](#TileMatrixSetLink) is the identifier of a [TileMatrixSet](#TileMatrixSet).

    * Check that the TileMatrixSet has either no [SupportedCRS](#SupportedCRS) element or one that matches the CRS identifier of one of the ETRS89 based or ITRS based coordinate systems.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4.7, Requirement 89

**Test type**: Manual

**Notes**

The multiplicity of this element is 0 or more.

This test is manual until a machine-readable "whitelist" register of the acceptable CRSes with their CRS identifiers and commonly used aliases ("label" and "URL" versions). To implement the test this kind on publicly available, official list must be established.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
TileMatrixSetLink <a name="TileMatrixSetLink"></a> | Contents/Layer/TileMatrixSetLink
TileMatrixSet <a name="TileMatrixSet"></a> | Contents/Layer/TileMatrixSet/ows:Identifier
SupportedCRS <a name="SupportedCRS"></a> | Contents/Layer/TileMatrixSet/ows:SupportedCRS
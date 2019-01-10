# Layer Coordinates Reference System

**Purpose**: Test that a supported CRS is provided based on ETRS89 for continental Europe and on ITRS outside continental Europe.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each named [Layer](#layer) element:

    * Check that at least one [CRS](#crs) element is provided stated explicitly or inherited from a parent Layer.

* Check manually if a geographical coordinate system based on ETRS89 is used in continental Europe or ITRS outside continental Europe.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.7, Requirement 40

**Test type**: Automated / Manual

**Notes**

The multiplicity of this element is 1 or more for each named layer stated explicitly or inherited from a parent Layer.

A Layer that contains a Named child element is a 'named Layer'.

This test cannot be fully implemented until a machine-readable "whitelist" register of the acceptable CRSes with their CRS identifiers and commonly used aliases ("label" and "URL" versions) is available. To implement the test, this kind of official list must be published.

A geographical coordinate system based on ETRS89 must be used in continental Europe and ITRS outside continental Europe. But it is not possible to know automatically if the layer belongs to continental Europe or not to decide which CRS shall be provided.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | wms:Capability/*/wms:Layer
CRS <a name="crs"></a> | wms:Capability/*/wms:Layer/wms:CRS

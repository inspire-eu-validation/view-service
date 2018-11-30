# Geographic BoundingBox

**Purpose**: Test that a Geographic Bounding Box is given for each Layer element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if there is exactly one [EX_GeographicBoundingBox](#EX_GeographicBoundingBox) node in each named Layer element or inherited from a parent Layer.

* Check manually that [EX_GeographicBoundingBox](#EX_GeographicBoundingBox) is the minimum bounding box for the data provided by the service.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.8, Requirement 19

**Test type**: Automated / Manual

**Notes**

The multiplicity of this element is 1 in each named Layer element stated explicitly or inherited from a parent Layer.

A Layer that contains a Named child element is a 'named Layer'.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
EX_GeographicBoundingBox <a name="EX_GeographicBoundingBox"></a> | wms:Capability/wms:Layer/wms:EX_GeographicBoundingBox
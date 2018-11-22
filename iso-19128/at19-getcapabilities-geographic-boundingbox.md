# Geographic BoundingBox

**Purpose**: Test that a Geographic Bounding Box is given for each Layer element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if there is a [EX_GeographicBoundingBox](#EX_GeographicBoundingBox) node in each Layer section of the Capabilities section.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.8, Requirement 19

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 in each Layer element.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
EX_GeographicBoundingBox <a name="EX_GeographicBoundingBox"></a> | wms:Capability/wms:Layer/wms:EX_GeographicBoundingBox
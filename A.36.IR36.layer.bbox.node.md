# A.36.IR36.layer.bbox.node

**Purpose**: This Layer metadata element shall be mapped to the wms:BoundingBox element. The minimum bounding rectangle of the area covered by the Layer in all supported CRS shall be given.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Check if there is a BoundingBox node in each Layer section for each CRS declared.

**Reference(s)**: 
* IR Annex III, Part A, Chapter 2.2.4
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.4.4

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
BoundingBox <a name="BoundingBox"></a> | /WMS_Capabilities/Capability/Layer/BoundingBox
Layer <a name="Layer"></a> | /WMS_Capabilities/Capability/Layer
CRS <a name="CRS"></a> | /WMS_Capabilities/Capability/Layer/BoundingBox/@CRS

# Bounding box in layer

**Purpose**: This Layer metadata element shall be mapped to the wms:BoundingBox element. The minimum bounding rectangle of the area covered by the Layer in all supported CRS shall be given.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)

**Test method**

* For each [CRS](#wmsCRS) that is listed for a specific [Layer](#Layer), check if there is a [BoundingBox](#BoundingBox) node in the same [Layer](#Layer) section with a corresponding attribute [@CRS](#CRS).

**Reference(s)**:

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), Chapter 4.2.3.3.4.4

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="Layer"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer
CRS <a name="wmsCRS"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:CRS
BoundingBox <a name="BoundingBox"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/BoundingBox
@CRS <a name="CRS"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/BoundingBox[@CRS]
